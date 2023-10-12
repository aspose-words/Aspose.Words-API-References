---
title: FieldTitle.Text
second_title: Aspose.Words för .NET API Referens
description: FieldTitle fast egendom. Hämtar eller ställer in texten i titeln.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

Hämtar eller ställer in texten i titeln.

```csharp
public string Text { get; set; }
```

### Exempel

Visar hur man använder fältet TITLE.

```csharp
Document doc = new Document();

 // Ställ in ett värde för den inbyggda dokumentegenskapen "Titel".
doc.BuiltInDocumentProperties.Title = "My Title";

// Vi kan använda fältet TITLE för att visa värdet på den här egenskapen i dokumentet.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// Ange ett värde för fältets textegenskap,
// och sedan uppdatera fältet kommer också att skriva över motsvarande inbyggda egenskap med det nya värdet.
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
* namnutrymme [Aspose.Words.Fields](../../fieldtitle/)
* hopsättning [Aspose.Words](../../../)


