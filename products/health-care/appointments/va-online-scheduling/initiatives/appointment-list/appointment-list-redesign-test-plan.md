# Manual-UI Test Plan - Appointment List Redesign 

## Project Summary Epic [#38062](https://app.zenhub.com/workspaces/vaos-team-603fdef281af6500110a1691/issues/gh/department-of-veterans-affairs/va.gov-team/38062) 
Looking to improve the user experience in VAOS by updating the appointment list page to help the veterans view their upcoming appointments, pending apppointments and past appointments. The goal is to have the VAOS appointments list show the same information and value as the equivalent list in MyHealtheVet.

## Business Rules (more details can be found [here](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/health-care/appointments/va-online-scheduling/engineering/vaos_business_rules.md#appointments-list))
On the VAOS homepage, the app displays the following for each status: 
- Upcoming appointments: displays up to 13 months of future booked VA and Community Care appointments including canceled VA and CC booked appointments 
- Pending requests: displays pending VA and Community Care appointment requests and prior 120 days of VA and Community Care canceled requests 
- Past appointments: displays up to 2 years of past VA and Community Care booked appointments (note: it does not display past canceled booked appointments) 

### Use Cases
 
- [ ] Use Case 1 - Validate upcoming appointments in VAOS 

     Configuration setup in test environment must include: 
  - [ ] Test user should have VA (in person, video visit and phone call) and Community Care booked appointments including canceled appointments

* **Description**
  - Tester will validate that they could view the list of their upcoming appointments (future appts) in VAOS 
    - [ ] Booked VA appointment - in person (at a Facility) 
    - [ ] Booked VA appointment - video connect (at a Facility) 
    - [ ] Booked VA appointment - video connect (at an ATLAS location) 
    - [ ] Booked VA appointment - video connect (at home, not a VA or ATLAS location) 
    - [ ] Booked VA appointment - phone call 
    - [ ] Booked Community Care appointment
    - [ ] Canceled VA appointment - in person (at a Facility) 
    - [ ] Canceled VA appointment - video connect (at a Facility) 
    - [ ] Canceled VA appointment - video connect (at an ATLAS location) 
    - [ ] Canceled VA appointment - video connect (at home, not a VA or ATLAS location) 
    - [ ] Canceled VA appointment - phone call 
    - [ ] Canceled Community Care appointment

- [ ] Use Case 2 - Validate pending requests in VAOS 

     Configuration setup in test environment must include: 
  - [ ] Test user should have VA and Community Care pending requests including canceled requests

* **Description**
  - Tester will validate that they could view the list of their pending requests in VAOS 
    - [ ] Pending VA request - in person (at a Facility) 
    - [ ] Pending Community Care request
    - [ ] Canceled VA request - in person (at a Facility) 
    - [ ] Canceled Community Care request

- [ ] Use Case 3 - Validate past appointments in VAOS

     Configuration setup in test environment must include: 
  - [ ] Test user should have past booked VA and Community Care appointments 

* **Description**
  - Tester will validate that they could view the list of their past booked appointments in VAOS 
    - [ ] Past booked VA appointment - in person (at a Facility) 
    - [ ] Past booked VA appointment - video connect (at a Facility) 
    - [ ] Past booked VA appointment - video connect (at an ATLAS location) 
    - [ ] Past booked VA appointment - video connect (at home, not a VA or ATLAS location) 
    - [ ] Past booked VA appointment - phone call 
    - [ ] Past booked Community Care appointment
 

### User flow
- [X] [Figma file](https://www.figma.com/file/xRs9s6QWoBPRhpdYCGc3cV/User-Flow?node-id=0%3A1&t=YhZr2QXznYwJ72lf-0) 

### Reference (if applicable) 
- [X] [Design file](https://www.figma.com/file/JpGM8LGBCqAlL8qh3DmFk8/Home-Page-Redesign?node-id=1172%3A81535&t=90yvScbbe8TiN61c-0)
- [X] [Copy doc](https://github.com/department-of-veterans-affairs/va.gov-team-sensitive/blob/master/Administrative/vagov-users/staging-test-accounts-vaos.md)

### Test Users 
- [X] [VAOS test users](https://github.com/department-of-veterans-affairs/va.gov-team-sensitive/blob/master/Administrative/vagov-users/staging-test-accounts-vaos.md)

### Summary Defect Report
- [ ] TBD 

### Traceability Report 
- [X] [VAOS](https://department-of-veterans-affairs.github.io/veteran-facing-services-tools/frontend-support-dashboard/unit-test-coverage-report/)

### E2E tests 
- [X] File path: `vets-website/src/applications/vaos/appointment-list/components/AppointmentsPageV2`
- [X] [Product's code link](https://github.com/department-of-veterans-affairs/vets-website/tree/main/src/applications/vaos/appointment-list/components/AppointmentsPageV2)

### Code coverage
- [X] File path: `vets-website/src/applications/vaos/appointment-list/components/AppointmentsPageV2`
- [X] [Product's code link](https://github.com/department-of-veterans-affairs/vets-website/tree/main/src/applications/vaos/appointment-list/components/AppointmentsPageV2)
