---
title: FieldComments.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: FieldComments Text fast egendom. Hämtar eller ställer in texten i kommentarerna i C#.
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

Visar hur du använder KOMMENTARER-fältet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in ett värde för dokumentets inbyggda egenskap "Kommentarer".
doc.BuiltInDocumentProperties.Comments = "My comment.";

// Skapa ett KOMMENTARER-fält för att visa värdet på den inbyggda egenskapen.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// Om vi ger COMMENTS-fältets Text-egenskapsvärde och uppdaterar det kommer fältet att göra det
// skriv över det aktuella värdet av den inbyggda "Kommentarer"-egenskapen med värdet av dess Text-egenskap,
// och visa sedan det nya värdet.
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
