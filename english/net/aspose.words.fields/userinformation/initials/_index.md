---
title: UserInformation.Initials
linktitle: Initials
articleTitle: Initials
second_title: Aspose.Words for .NET
description: Discover how to use the UserInformation Initials property to easily manage and customize user initials for enhanced personalization and user experience.
type: docs
weight: 40
url: /net/aspose.words.fields/userinformation/initials/
---
## UserInformation.Initials property

Gets or sets the user's initials.

```csharp
public string Initials { get; set; }
```

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
Assert.That(builder.InsertField(" USERNAME ").Result, Is.EqualTo(userInformation.Name));
Assert.That(builder.InsertField(" USERINITIALS ").Result, Is.EqualTo(userInformation.Initials));
Assert.That(builder.InsertField(" USERADDRESS ").Result, Is.EqualTo(userInformation.Address));

// The field options object also has a static default user that fields from all documents can refer to.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.That(builder.InsertField(" USERNAME ").Result, Is.EqualTo("Default User"));
Assert.That(builder.InsertField(" USERINITIALS ").Result, Is.EqualTo("D. U."));
Assert.That(builder.InsertField(" USERADDRESS ").Result, Is.EqualTo("One Microsoft Way"));

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

### See Also

* class [UserInformation](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
