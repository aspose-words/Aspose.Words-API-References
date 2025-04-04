---
title: UserInformation.defaultUser property
linktitle: defaultUser property
articleTitle: defaultUser property
second_title: Aspose.Words for Node.js
description: "UserInformation.defaultUser property. Default user information."
type: docs
weight: 30
url: /nodejs-net/aspose.words.fields/userinformation/defaultUser/
---

## UserInformation.defaultUser property

Default user information.


```js
get defaultUser(): Aspose.Words.Fields.UserInformation
```

### Remarks

Use the [FieldOptions.currentUser](../../fieldoptions/currentUser/) property to specify user information for single document.



### Examples

Shows how to set user details, and display them using fields.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a UserInformation object and set it as the data source for fields that display user information.
let userInformation = new aw.Fields.UserInformation();
userInformation.name = "John Doe";
userInformation.initials = "J. D.";
userInformation.address = "123 Main Street";
doc.fieldOptions.currentUser = userInformation;

// Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
// the respective properties of the UserInformation object that we have created above.
expect(builder.insertField(" USERNAME ").result).toEqual(userInformation.name);
expect(builder.insertField(" USERINITIALS ").result).toEqual(userInformation.initials);
expect(builder.insertField(" USERADDRESS ").result).toEqual(userInformation.address);

// The field options object also has a static default user that fields from all documents can refer to.
aw.Fields.UserInformation.defaultUser.name = "Default User";
aw.Fields.UserInformation.defaultUser.initials = "D. U.";
aw.Fields.UserInformation.defaultUser.address = "One Microsoft Way";
doc.fieldOptions.currentUser = aw.Fields.UserInformation.defaultUser;

expect(builder.insertField(" USERNAME ").result).toEqual("Default User");
expect(builder.insertField(" USERINITIALS ").result).toEqual("D. U.");
expect(builder.insertField(" USERADDRESS ").result).toEqual("One Microsoft Way");

doc.updateFields();
doc.save(base.artifactsDir + "FieldOptions.currentUser.docx");
```

### See Also

* module [Aspose.Words.Fields](../../)
* class [UserInformation](../)

