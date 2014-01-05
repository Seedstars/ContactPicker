# ContactPicker plugin for Cordova / PhoneGap

This Plugin is inspired from ContactChooser plugin [here](https://github.com/monday-consulting/ContactChooser)

This Plugin brings up a native iOS or Android contact-picker overlay, accessing the addressbook and returning the selected contact's name and email, also new contact can be added.
## Usage

This has been successfully tested from Cordova 2.2.0 through to version 3.1.0.

Example Usage: 

1. **Pick contact**

```js
window.plugins.ContactPicker.chooseContact(function(contactInfo) {
    alert(contactInfo.displayName + " " + contactInfo.email);
});
```

The method which will return a JSON. Example:

```json
{
    displayName: "John Doe",
    email: "john.doe@mail.com"
}
```
2. **Add new contact**

```js
ContactPicker.prototype.addContact = function(success, failure){
    cordova.exec(success, failure, "ContactPicker", "addContact", []);
};
```

## MIT Licence

Copyright 2013 Monday Consulting GmbH

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
