
## CHIP/LoROTA/Clinician Workflow/Vista-api performance testing

![CHIP/CW/VistA API subsystem](./subsystems/subsystem_chip_cw_vista-api-container-diagram.png "CHIP/CW/VistA API subsystem")

### Test Environment

CHIP and LoROTA lambdas run from VAEC AWS account. Clincian Workflow runs as an ECS service, also in VAEC account. VistA api is run on on-prem instances.

### Load Estimates
CHIP and LoROTA endpoints are called by VEText during initiation of check-in and pre check-in scenarios, as well as vets-api during these scenarios.

Based on the data on appointments for the week of 4/22, we estimate a load of about 35k check-ins per hour assuming all stations have mobile check-in enabled and all appointments go through mobile check-in. See [Load Estimates](readme.md#load-estimates) for more details.

Based on the outgoing twilio messages and assuming the same load for mobile pre check-in reminders, we have an upper range of about 145k pre check-in hourly reminders.

### Tools
We're currently looking into both [locust](https://locust.io/) and [K6](https://k6.io/open-source) for scripting and load generation. We will finalize the tool based on the ease of script creation, ease of setup/install in VAEC cloud and the ability to generate the desired load profile.

### Load Profile

Based on the load of 35,260 check-ins per hour, and 145,000 pre check-ins per hour, the load profile for CHIP lambdas is below:

| endpoint            | requests per min |
|---------------------|------------------|
| initiateCheckIn     | 588              |
| refreshAppointments | 588              |
| checkIn             | 588              |
| initiatePreCheckin  | 2417             |
| refreshPreCheckin   | 2417             |


### Test Data Generation
Shane has created a node script to generate test appointments in VistA: https://github.com/shanemelliott/createAppts

### Monitoring

We will use DataDog to monitor system performance and resource utilization during the load test execution. We will also monitor CloudWatch resources as well as error logs.

Clinician Workflow: https://tevi.ddog-gov.com/dashboard/bap-942-8fb/technical-dashboard---clinician-workflow

CHIP (nonprod): https://tevi.ddog-gov.com/dashboard/hcd-qby-eqm/technical-dashboard---chip-nonprod

LoROTA:

VistA API dashboard (Dev): https://tevi.ddog-gov.com/dashboard/cim-s7k-5s5/vista-api-dev

VistA API dashboard (Staging):
