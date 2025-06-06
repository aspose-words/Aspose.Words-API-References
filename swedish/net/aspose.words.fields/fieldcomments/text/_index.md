---
title: FieldComments.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Hantera dina kommentarer enkelt med egenskapen FieldComments Text – hämta eller ställ enkelt in kommentarstext för förbättrad användarinteraktion.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

Hämtar eller ställer in texten i kommentarerna.

```csharp
public string Text { get; set; }
```

## Exempel

Visar hur man använder KOMMENTAR-fältet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange ett värde för dokumentets inbyggda egenskap "Kommentarer".
doc.BuiltInDocumentProperties.Comments = "My comment.";

// Skapa ett KOMMENTARER-fält för att visa värdet för den inbyggda egenskapen.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// Om vi anger KOMMENTARER-fältets egenskapsvärde Text och uppdaterar det, kommer fältet att
// skriv över det aktuella värdet för den inbyggda egenskapen "Kommentarer" med värdet för dess Text-egenskap,
// och sedan visa det nya värdet.
field.Text = "My overriding comment.";
field.Update();

Assert.AreEqual(" COMMENTS  \"My overriding comment.\"", field.GetFieldCode());
Assert.AreEqual("My overriding comment.", field.Result);

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### Se även

* class [FieldComments](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
