---
title: FieldTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Hantera din FieldTitle Text-egenskap enkelt. Hämta eller ställ enkelt in titeltext för förbättrad tydlighet och användarupplevelse i din applikation.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

Hämtar eller ställer in titelns text.

```csharp
public string Text { get; set; }
```

## Exempel

Visar hur man använder fältet TITEL.

```csharp
Document doc = new Document();

 // Ange ett värde för den inbyggda dokumentegenskapen "Titel".
doc.BuiltInDocumentProperties.Title = "My Title";

// Vi kan använda fältet TITLE för att visa värdet för den här egenskapen i dokumentet.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// Anger ett värde för fältets Text-egenskap,
// och att sedan uppdatera fältet kommer även att skriva över motsvarande inbyggda egenskap med det nya värdet.
builder.Writeln();
field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Text = "My New Title";
field.Update();

Assert.AreEqual(" TITLE  \"My New Title\"", field.GetFieldCode());
Assert.AreEqual("My New Title", field.Result);
Assert.AreEqual("My New Title", doc.BuiltInDocumentProperties.Title);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TITLE.docx");
```

### Se även

* class [FieldTitle](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
