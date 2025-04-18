---
title: FieldUserAddress.UserAddress
linktitle: UserAddress
articleTitle: UserAddress
second_title: Aspose.Words for .NET
description: Manage user postal addresses effortlessly with the FieldUserAddress property. Easily retrieve and update current user information for enhanced experience.
type: docs
weight: 20
url: /net/aspose.words.fields/fielduseraddress/useraddress/
---
## FieldUserAddress.UserAddress property

Gets or sets the current user's postal address.

```csharp
public string UserAddress { get; set; }
```

## Examples

Shows how to use the USERADDRESS field.

```csharp
Document doc = new Document();

// Create a UserInformation object and set it as the source of user information for any fields that we create.
UserInformation userInformation = new UserInformation();
userInformation.Address = "123 Main Street";
doc.FieldOptions.CurrentUser = userInformation;

// Create a USERADDRESS field to display the current user's address,
// taken from the UserInformation object we created above.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserAddress fieldUserAddress = (FieldUserAddress)builder.InsertField(FieldType.FieldUserAddress, true);
Assert.AreEqual(" USERADDRESS ", fieldUserAddress.GetFieldCode());
Assert.AreEqual("123 Main Street", fieldUserAddress.Result);

// We can set this property to get our field to override the value currently stored in the UserInformation object.
fieldUserAddress.UserAddress = "456 North Road";
fieldUserAddress.Update();

Assert.AreEqual(" USERADDRESS  \"456 North Road\"", fieldUserAddress.GetFieldCode());
Assert.AreEqual("456 North Road", fieldUserAddress.Result);

// This does not affect the value in the UserInformation object.
Assert.AreEqual("123 Main Street", doc.FieldOptions.CurrentUser.Address);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERADDRESS.docx");
```

### See Also

* class [FieldUserAddress](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
