# javaScript-good-practices
JavaScript Coding Standard Guidelines:

This Document will cover following topics:
Commenting Code
Naming Convention
Whitespaces
Line length
Chain Method call
Some awareness

Commenting Code
Javascript comment is used to explain Javascript code and more readable. Comment code all point of interest, describe why and not what.

Comments are always preceded by a blank line. Comments start with a capital first letter, but don't require a period at the end, unless you're writing full sentences. There must be a single space between the comment token and the comment text.

use //
Single line comments are used to comment single line of code.
// set default menu to home
	var menu = this.menu || "Home";
use /******/
Multi-line comments are used to comment at the beginning of file and function.
/**
 * Adds two numbers
 * @param {Number} a 
 * @param {Number} b
 * @return {Number} sum
 */
 function sum(a,b) { 
   return a + b;
 }

use // TODO: 
To define a solution of an existing problem or to suggest a solution that needs to be implemented.
Backbone.View.extend({ 
 initialize: function () {

 // TODO: setInterval should be configurable by an options param
  this.setInterval = 0;
 }
});
use // FIXME: 
To point out a problem use // FIXME:
Backbone.View.extend({ 
 initialize: function () {

 // FIXME: shouldn't use a global here
  setInterval = 0;
 }
});

Naming Convention
Avoid single letter names. Variable, function and file/ module name should be meaningful word.

js library/ utility
Use all lowercase for file naming. Don’t use any space in filename. 
product-name[.plugin][-version][.filetype].js
First part is mandatory and it should be meaningful name. second and third part is optional.
Example:
 
jquery-1.4.2.min.js
jquery.plugin-0.1.js
jquery-ui-1.10.3.custom.min.js
jquery.dataTables.bootstrap.min.js

Controller Name
Use camelcase for controller naming.
UserController.js

Model Name
Use camelcase for Model naming.
UserModel.js

Schema Name
Use camelcase for schema naming.
UserSchema.js

View/ template/ collection
Use lowercase for filename and use underscore to separate the word.
create_user_view.js
create_user_view.html
users_collection.js

Class/ Module Name
Use pascalcase for class/ module name.
module.exports = mongoose.model('User', UserSchema);
	//Here User is a valid model name. 

var User = require('../models/UserModel')();
	\\Here User is a valid name for require.


Variables
Use camelcase for variable naming and also use full word where possible
firstName, price

Functions
Use camelcase for function naming. 
getTotal(), getUserData()

URL hash/ API
use all lowercase in url and api and words are separated by underscore.
http://localhost/users
	http://localhost/get_users
	http://localhost/api/get_user_data


