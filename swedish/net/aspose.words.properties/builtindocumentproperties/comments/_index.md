---
title: BuiltInDocumentProperties.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words för .NET
description: Hantera dina dokumentkommentarer enkelt med BuiltInDocumentProperties. Hämta eller ställ enkelt in kommentarer för förbättrat samarbete och tydlighet.
type: docs
weight: 60
url: /sv/net/aspose.words.properties/builtindocumentproperties/comments/
---
## BuiltInDocumentProperties.Comments property

Hämtar eller ställer in dokumentkommentarer.

```csharp
public string Comments { get; set; }
```

## Exempel

Visar hur man arbetar med inbyggda dokumentegenskaper i kategorin "Beskrivning".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Nedan följer fyra inbyggda dokumentegenskaper som har fält som kan visa sina värden i dokumentets brödtext.
// 1 - Egenskapen "Author", som vi kan visa med hjälp av ett AUTHOR-fält:
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - Egenskapen "Titel", som vi kan visa med hjälp av ett TITEL-fält:
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - Egenskapen "Ämne", som vi kan visa med ett ÄMNE-fält:
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - Egenskapen "Kommentarer", som vi kan visa med hjälp av ett KOMMENTARER-fält:
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// Den inbyggda egenskapen "Kategori" har inget fält som kan visa dess värde.
properties.Category = "My category";

// Vi kan ange flera nyckelord för ett dokument genom att separera strängvärdet för egenskapen "Nyckelord" med semikolon.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// Vi kan högerklicka på det här dokumentet i Utforskaren och hitta dessa egenskaper i "Egenskaper" -> "Detaljer".
// Den inbyggda egenskapen "Författare" finns i gruppen "Ursprung", och de andra finns i gruppen "Beskrivning".
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### Se även

* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
