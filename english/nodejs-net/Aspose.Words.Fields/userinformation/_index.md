---
title: UserInformation class
linktitle: UserInformation class
articleTitle: UserInformation class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.UserInformation class. Specifies information about the user"
type: docs
weight: 1310
url: /nodejs-net/Aspose.Words.Fields/userinformation/
---

## UserInformation class

Specifies information about the user.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/nodejs-net/working-with-fields/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [UserInformation()](./UserInformation/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [address](./address/) | Gets or sets the user's postal address. |
| [defaultUser](./defaultUser/) | Default user information. |
| [initials](./initials/) | Gets or sets the user's initials. |
| [name](./name/) | Gets or sets the user's name. |

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

* module [Aspose.Words.Fields](../)

