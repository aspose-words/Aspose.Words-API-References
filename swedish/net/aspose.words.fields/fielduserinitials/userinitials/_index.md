---
title: FieldUserInitials.UserInitials
linktitle: UserInitials
articleTitle: UserInitials
second_title: Aspose.Words för .NET
description: Få åtkomst till och anpassa egenskapen FieldUserInitials för att enkelt hantera användarinitialer, vilket förbättrar anpassningen och användarupplevelsen.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

Hämtar eller ställer in den aktuella användarens initialer.

```csharp
public string UserInitials { get; set; }
```

## Exempel

Visar hur man använder fältet ANVÄNDARINITIALS.

```csharp
Document doc = new Document();

// Skapa ett UserInformation-objekt och ange det som källa för användarinformation för alla fält som vi skapar.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Skapa ett fält ANVÄNDARINITIALS för att visa den aktuella användarens initialer,
// hämtad från UserInformation-objektet som vi skapade ovan.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

 // Vi kan ställa in den här egenskapen så att vårt fält åsidosätter det värde som för närvarande lagras i UserInformation-objektet.
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// Detta påverkar inte värdet i UserInformation-objektet.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### Se även

* class [FieldUserInitials](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
