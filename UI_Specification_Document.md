# New User Page
***
### Introduction
This page contains 3 different containers. First one is the "Header Container" and it has control elements to control containers which are standing side by side under the header. The left container under the header is "User Details Container" and it will contain the details as table in itself. The right container under the header is "New User Form Container" and it has text description with edittexts. 
***
#### Header Container
The header will be at the top without any margin from top, left and right. Its background color will be `#E2E2E2` (gray). It will contain 4 different elements:
1. New User Button (Refer to [Material Design](https://material.io/develop/web) Buttons)
    + Background-color: `#0C59F3` (blue)
    + icon: plus-icon
    + icon-color: `#FFFFFF` (white)
    + text: "New User"
    + text-color: `#FFFFFF` (white)
    + margin-left: `16px`
2. Checkbox
	+ color: `#0C59F3` (blue)
	+ checkcolor: `#FFFFFF` (white)
	+ margin-left: `16px`
3. Checkbox Text
	+ text: "Hide Disabled User"
	+ text-color: `#000000` (black)
4. Save User Button (Refer to [Material Design](https://material.io/develop/web) Buttons)
	+ Background-color: `#0C59F3` (blue)
    + text: "Save User"
    + text-color: `#FFFFFF` (white)
    + margin-right: `16px`
The height of the header part will be the wrap-content. And there will be `8px` margin from top and bottom to make it more readable. 
***
#### User Details Container
In this section viewer of this page will see the saved user information as a table. This table will have 4 different columns. The column names are as follows respectively "ID", "User Name", "Email" and "Enabled". Constraints for this container like in below:
+ margin-top: `16px`
+ margin-left: `4px` 
The features of the first row is specified in below:
+ background-color: `#0C59F3` (blue)
+ text-color: `#FFFFFF` (white)

Near all columns there will be two different icons. The first icon is arrow drop up and down for ranking and the second one is filter icon. The icons can be found in [material icons](https://material.io/resources/icons/?style=baseline) site. 

The other rows for each user details, *known as records in database*, has different backgrounds one by one. First record has white background and the other row's background is light-blue (`#81CCFF`). And for other records background colors will change one by one.
***
#### New User Form Container
In this container there are several edittext with explaining text in front of them. These are the user's information that will be registered. The constraints of container is in below: 
+ margin-top: `16px`
+ margin-right: `4px` 

At the top of form there will be a header. The features of header is like that:
+ background-color: `#E2E2E2` (gray)
+ text-color: `#000000` (black)
+ text: "New User"

After specifying header of form container the edittext form elements needs to be designed one under the other.
1. Username
	+ text: "Username: "
	+ text-color: `#000000` (black)
	+ margin-top: `16px`
	+ edittext: blank
2. Display Name
	+ text: "Display Name: "
	+ text-color: `#000000` (black)
	+ margin-top: `16px`
	+ edittext: blank
3. Phone
	+ text: "Phone: "
	+ text-color: `#000000` (black)
	+ margin-top: `16px`
	+ edittext: blank
4. Email
	+ text: "Email: "
	+ text-color: `#000000` (black)
	+ margin-top: `16px`
	+ edittext: blank
5. User Roles
	+ text: "User Roles: "
	+ text-color: `#000000` (black)
	+ margin-top: `16px`
	+ edittext-hint: "Select user roles"

	There will be drop-down menu for this edittext click. The options for drop-down menu will be : "Guest","Admin" and "SuperAdmin".

6. Enabled
	+ checkbox
***
All definitions for elements explanied in above. The functionality will be specified in the functionality and error section
### Functionality and Error Check
When a person open this page only the "new user" button at header container has to be enabled and other buttons and edittexts have to be disabled. And "save user" button's background has to be %50 transparent.

After "new user" button has clicked then disabled buttons become enabled to fill the form containers element to save new user. 

If any of edittext is empty or not written in proper way then a red warning error appears. If all required edittexts are filled in proper way and save button has clicked then details container needs to be refreshed and new user can be seen in here. After that the state of buttons turn to be start position. So just "new user" button will be enabled and others disabled again. 