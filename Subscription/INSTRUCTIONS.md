1. Navigate to Subscription Management > Subscription Management
2. Select Subscriptions tab
3. Open any Per-User type Subscription
4. Under Subscribed Groups, select Add groups
5. Select All groups
6. Refresh Browser screen
7. Select the Subscribed Users tab or access the User Subscription [user_has_subscription] table

NOTE:
- Each Subscription record is associated to certain roles which is all stored in the sn_sub_man_license_application_roles table
- Filter on the sn_sub_man_license_application_roles table for the Subscription Entitlement, and ensure the Role Type field matches the Measured role types field on the Subscription
     - sn_sub_man_license_application_roles.sr_license_role_type = subscriptionEntitlementGR.measured_role_types.id
- This is deemed the list of {Valid Associated Roles}
- Navigate to the User Roles [sys_user_has_role] table
     - Apply the following filters:
       Role.Name is one of {Valid Associated Roles}
       AND User.Active is true
       AND User.Last Login Time is relative after 365 Days ago
     - Group By User 
