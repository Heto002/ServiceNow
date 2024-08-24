Action Name: Cart API

Action Input
  - Catalog Item | catalog_item | Reference.Catalog Item
  - Quantity | quantity | Integer
  - Variables |  variables | Array.Object

Script Step
Input Variables
  - catalog_item_sys_id | {{Input Variables.catalog_item.sys_id}}
  - quantity | {{Input Variables.quantity}}
  - variables | {{Input Variables.variables}}
Script
  **See CART JS file**
Output Variables
  - Request Number | request_number | String

Action Output
  - Request Number | request_number | String | {{Script Step.request_number}}
