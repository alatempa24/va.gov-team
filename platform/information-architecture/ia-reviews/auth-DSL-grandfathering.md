# Login.gov Grandfathering IA Spec Doc
**STATUS: Draft**
- Edit history:
  - 3/7/23 - KO draft

**Team:** [Login.gov Adoption](https://github.com/department-of-veterans-affairs/va.gov-team/tree/master/products/login.gov-adoption)

**IA Request:** [Link to Sitewide Content and IA intake request](https://app.zenhub.com/workspaces/sitewide-content-accessibility-and-ia-63a1d63232beba0011a7833f/issues/gh/department-of-veterans-affairs/va.gov-team/52754)

**On this page:**
- [User/page flows](#flows)
- [Page structure](#map)
- [URLs and breadcrumbs](#url)
- [Entry points](#nav)
- [Redirects](#redirects)
- [Meeting notes](#notes)


## <a name="flows"></a>User/page flows <br>

Latest at this mural: https://app.mural.co/t/departmentofveteransaffairs9999/m/departmentofveteransaffairs9999/1676397151510/f4cf4f4187a3d0fd5f2d6d56c9bd2ba3a4376e7a?sender=ua67f17f1c416a96ea04d2476

![User voluntarily starts account transfer process online](https://user-images.githubusercontent.com/122126772/223573083-96df6adc-3d3c-4953-89aa-467e0c63d985.png)

![User interrupted during online task to do optional account transfer](https://user-images.githubusercontent.com/122126772/223573085-425087a4-69ed-4025-8c61-ff5d0a11d845.png)



## <a name="url"></a>Page structure
- any new pages for this flow will be under the Root, and will not be indexable by search engines (at least for this grandfathering flow)


## <a name="url"></a>URLs and breadcrumbs


**1) Link Account Info Page - New**
- URL:  TBD pending content, but an idea is (va.gov/account-transition). It would be ideal if this page could be reused for the MHV transition too.
- Breadcrumb: none needed
- Notes: Becaused we don't want this page discoverable by search enginers, we also need to tag the page as 'no index', and make sure it doesn't go into the xml sitemap. Your engineers should know what this means, but let us know if you have any Qs. 

**2) Account Linking Error Page - New**
- URL:  TBD pending content
- Breadcrumb: none needed
- Notes: Becaused we don't want this page discoverable by search enginers, we also need to tag the page as 'no index', and make sure it doesn't go into the xml sitemap. Your engineers should know what this means, but let us know if you have any Qs.


## <a name="nav"></a>Entry points <br>

1.  TBD, but probably not --> we might need to add something to the SSO page as the Sept 30th deadline approaches, but that is not getting figured out before midpoint.


## <a name="redirects"></a>Redirects <br>
*A list of any critical redirects needed as part of this product/feature launch. Redirects are required for any URL changes to ensure visitors do not receive a 404 - Page not found error in the experience. For any redirects listed, please submit a request for the redirect using the [Redirect Request Issue Template](https://github.com/department-of-veterans-affairs/va.gov-team/issues/new?assignees=mnorthuis&labels=content-ia-team%2C+ia&template=redirect-request.md&title=Redirect+Request) at least 2 weeks in advance.*  


Current URL | Redirect to | Notes

TBD

<hr>

## <a name="notes"></a>Open Questions
1. Ask the other auth team: whether we can send the user directly to the DSL sign-in page, rather than the SSO modal, so that the user doesn't accidentally exit the flow. Also recognition vs recall --> if we send them to SSO from the email, we're asking them to remember what they were supposed to do on this page. Sending them directly from the email to the DSL login page could prevent workflow dropout.
2. User test: experience of going directly to DSL sign-in vs SSO modal --> if we do the above, are there any risks for the user?
3. Figure out: What should we do if the user is logged out of VA.gov while they are on Login.gov/ID.me?
4. Figure out: What do we do if the user arrives at this workflow but they've already done the linking?
5. Figure out: For the interrupted flow, how do we make sure the user can return to the task they were originally trying to do?
6. Map: post-september 30th flows for veterans that did NOT do the bind in time
