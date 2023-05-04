---
title: FieldUserInitials.UserInitials
linktitle: UserInitials
articleTitle: UserInitials
second_title: Aspose.Words for .NET
description: FieldUserInitials UserInitials property. Gets or sets the current users initials in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

Gets or sets the current user's initials.

```csharp
public string UserInitials { get; set; }
```

## Examples

Shows how to use the USERINITIALS field.

```csharp
Document doc = new Document();

// Create a UserInformation object and set it as the source of user information for any fields that we create.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Create a USERINITIALS field to display the current user's initials,
// taken from the UserInformation object we created above.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

// We can set this property to get our field to override the value currently stored in the UserInformation object. 
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// This does not affect the value in the UserInformation object.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### See Also

* class [FieldUserInitials](../)
* namespace [Aspose.Words.Fields](../../fielduserinitials/)
* assembly [Aspose.Words](../../../)
