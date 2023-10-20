---
title: FieldBibliography.FormatLanguageId
linktitle: FormatLanguageId
articleTitle: FormatLanguageId
second_title: Aspose.Words för .NET
description: FieldBibliography FormatLanguageId fast egendom. Hämtar eller ställer in språkID som används för att formatera de bibliografiska källorna i dokumentet i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldbibliography/formatlanguageid/
---
## FieldBibliography.FormatLanguageId property

Hämtar eller ställer in språk-ID som används för att formatera de bibliografiska källorna i dokumentet.

```csharp
public string FormatLanguageId { get; set; }
```

## Exempel

Visar hur man arbetar med CITATION och BIBLIOGRAPHY-fält.

```csharp
// Öppna ett dokument som innehåller bibliografiska källor som vi kan hitta i
// Microsoft Word via referenser -> Citat & Bibliografi -> Hantera källor.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Skapa ett citat med bara sidnumret och författaren till den refererade boken.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Vi hänvisar till källor med deras taggnamn.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Skapa ett mer detaljerat citat som citerar två källor.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Vi kan använda ett BIBLIOGRAFI-fält för att visa alla källor i dokumentet.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Se även

* class [FieldBibliography](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
