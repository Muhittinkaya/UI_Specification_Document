# Behavior of Components
***
There is 2 cases while viewer wants to view this page. 
1. There is no problem on network
2. There is a problem with network whether server problem or loss of internet connection.

* If there is a problem with network then viewer will just see an error message on top-left of page like **"There is a problem on network, please try again later!"**
* If first case happens then page will load normally as it can be seen in image given in readme. 
***
When viewer enters the page he/she can only be able to click "new user" button. **New User Form Container**'s all elements will be disabled until viewer clicks "new user" button on Header Container. 
* If viewer clicks then a snackbar message will appear as **"Please click 'new user' button at the top."** 
* If there is at least one record in database then it will be shown in **User Details Container**'s table. But if there is no record then there will be a message in this container like **"There is no record saved."**

#### Header Component's Behavior
***
At first only the "new user" button and "Hide Disabled User" checkbox will be clickable but "save user" button won't be clickable and it will be 50% transparent.
* If viewer of the page clicks "new user" button then a `ripple effect` appears then **New User Form Container** becomes enabled to fill edittexts and click checkbox.
* When "Hide Disabled User" checkbox is clicked then **User Details Container** will be refreshed and disabled user will appear in the container.
* "Save user" button is disabled until new user form is filled appropriately. If form is filled in right way then this button will be enabled.

#### New User Form Container
***
As it is described above if viewer not clicked "new user" button then this container won't be editable. If viewer clicks that button then this container's all element becomes editable and clickable.
* The viewer can edit the areas "username" and "display name" only with alphabetic characters, not numerics.
* The phone area just can be numeric characters and there has to be 10 numbers according to Turkish phone numbers.
* There has to be `'@'` sign in the email and `'.com'` at the end of the email.
* Viewer has to select one of the drop-down menu elements.
* Enabled checkbox is optional to click. It effects the **User Details** table and if viewer clicks **Hide Disabled User** then all users will be seen at the table.

**NOTE:** If there is an empty edittext or not selected menu element in this part then that part's border will be red and there will be an error message on that edittext.
If all elements are filled in the right way then viewer can click "save user" button at the top right. The form data will be loaded into database.
After clicking "save user" button then all container disables again.

#### User Details Container
***
Viewer just can click two different images in this part: Drop-up arrows and filter images. The table is read-only not changable in here. 
* When viewer clicks arrow then the table will be ordered ascending or descending.
* When viewer clicks filter then a small textbox will open to filter text to search.
* When user not clicks "Hide Disabled User" then all users will be shown in here.
* If there is a problem on database server then an error message will appear on this part as "An error occured in server!".