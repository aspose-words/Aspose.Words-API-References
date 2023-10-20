---
title: BuiltInDocumentProperties.Subject
linktitle: Subject
articleTitle: Subject
second_title: Aspose.Words för .NET
description: BuiltInDocumentProperties Subject fast egendom. Hämtar eller ställer in ämnet för dokumentet i C#.
type: docs
weight: 260
url: /sv/net/aspose.words.properties/builtindocumentproperties/subject/
---
## BuiltInDocumentProperties.Subject property

Hämtar eller ställer in ämnet för dokumentet.

```csharp
public string Subject { get; set; }
```

## Exempel

Visar hur man arbetar med inbyggda dokumentegenskaper i kategorin "Beskrivning".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Nedan finns fyra inbyggda dokumentegenskaper som har fält som kan visa sina värden i dokumentets brödtext.
// 1 - "Author"-egenskap, som vi kan visa med ett AUTHOR-fält:
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - Egenskapen "Titel", som vi kan visa med ett TITLE-fält:
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - "Subject"-egenskap, som vi kan visa med ett SUBJECT-fält:
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - "Comments"-egenskapen, som vi kan visa med ett KOMMENTAR-fält:
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// Den inbyggda egenskapen "Kategori" har inte ett fält som kan visa dess värde.
properties.Category = "My category";

// Vi kan ställa in flera nyckelord för ett dokument genom att separera strängvärdet för egenskapen "Keywords" med semikolon.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// Vi kan högerklicka på det här dokumentet i Utforskaren och hitta dessa egenskaper i "Egenskaper" -> "Detaljer".
// Den inbyggda "Author"-egenskapen är i gruppen "Origin" och de andra är i gruppen "Description".
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### Se även

* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
