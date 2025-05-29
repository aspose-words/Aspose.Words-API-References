---
title: FieldUserName.UserName
linktitle: UserName
articleTitle: UserName
second_title: Aspose.Words för .NET
description: Hantera den aktuella användarens namn enkelt med egenskapen FieldUserName. Förbättra användarupplevelsen och personifiera interaktioner sömlöst.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

Gest eller anger den aktuella användarens namn.

```csharp
public string UserName { get; set; }
```

## Exempel

Visar hur man använder fältet ANVÄNDARNAMN.

```csharp
Document doc = new Document();

// Skapa ett UserInformation-objekt och ange det som källa för användarinformation för alla fält som vi skapar.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett ANVÄNDARNAMN-fält för att visa den aktuella användarens namn,
// hämtad från UserInformation-objektet som vi skapade ovan.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 // Vi kan ställa in den här egenskapen så att vårt fält åsidosätter det värde som för närvarande lagras i UserInformation-objektet.
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// Detta påverkar inte värdet i UserInformation-objektet.
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### Se även

* class [FieldUserName](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
