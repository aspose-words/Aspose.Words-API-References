---
title: FieldUserAddress.UserAddress
linktitle: UserAddress
articleTitle: UserAddress
second_title: Aspose.Words för .NET
description: Hantera användarnas postadresser enkelt med egenskapen FieldUserAddress. Hämta och uppdatera enkelt aktuell användarinformation för en förbättrad upplevelse.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fielduseraddress/useraddress/
---
## FieldUserAddress.UserAddress property

Hämtar eller ställer in den aktuella användarens postadress.

```csharp
public string UserAddress { get; set; }
```

## Exempel

Visar hur man använder fältet ANVÄNDARADRESS.

```csharp
Document doc = new Document();

// Skapa ett UserInformation-objekt och ange det som källa för användarinformation för alla fält som vi skapar.
UserInformation userInformation = new UserInformation();
userInformation.Address = "123 Main Street";
doc.FieldOptions.CurrentUser = userInformation;

// Skapa ett fält ANVÄNDARADRESS för att visa den aktuella användarens adress,
// hämtad från UserInformation-objektet som vi skapade ovan.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserAddress fieldUserAddress = (FieldUserAddress)builder.InsertField(FieldType.FieldUserAddress, true);
Assert.AreEqual(" USERADDRESS ", fieldUserAddress.GetFieldCode());
Assert.AreEqual("123 Main Street", fieldUserAddress.Result);

// Vi kan ställa in den här egenskapen så att vårt fält åsidosätter det värde som för närvarande lagras i UserInformation-objektet.
fieldUserAddress.UserAddress = "456 North Road";
fieldUserAddress.Update();

Assert.AreEqual(" USERADDRESS  \"456 North Road\"", fieldUserAddress.GetFieldCode());
Assert.AreEqual("456 North Road", fieldUserAddress.Result);

// Detta påverkar inte värdet i UserInformation-objektet.
Assert.AreEqual("123 Main Street", doc.FieldOptions.CurrentUser.Address);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERADDRESS.docx");
```

### Se även

* class [FieldUserAddress](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
