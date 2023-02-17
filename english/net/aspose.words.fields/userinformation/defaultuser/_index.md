---
title: UserInformation.DefaultUser
second_title: Aspose.Words for .NET API Reference
description: UserInformation property. Default user information in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/userinformation/defaultuser/
---
## UserInformation.DefaultUser property

Default user information.

```csharp
public static UserInformation DefaultUser { get; }
```

## Remarks

Use the [`CurrentUser`](../../fieldoptions/currentuser/) property to specify user information for single document.

## Examples

Shows how to set user details, and display them using fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a UserInformation object and set it as the data source for fields that display user information.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
// the respective properties of the UserInformation object that we have created above. 
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// The field options object also has a static default user that fields from all documents can refer to.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

### See Also

* class [UserInformation](../)
* namespace [Aspose.Words.Fields](../../userinformation/)
* assembly [Aspose.Words](../../../)
