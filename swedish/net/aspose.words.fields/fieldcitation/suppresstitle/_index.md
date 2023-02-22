---
title: FieldCitation.SuppressTitle
second_title: Aspose.Words för .NET API Referens
description: FieldCitation fast egendom. Hämtar eller ställer in om titelinformationen undertrycks från citatet.
type: docs
weight: 90
url: /sv/net/aspose.words.fields/fieldcitation/suppresstitle/
---
## FieldCitation.SuppressTitle property

Hämtar eller ställer in om titelinformationen undertrycks från citatet.

```csharp
public bool SuppressTitle { get; set; }
```

### Exempel

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
fieldBibliography.FormatLanguageId = "1124";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 1124", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Se även

* class [FieldCitation](../)
* namnutrymme [Aspose.Words.Fields](../../fieldcitation/)
* hopsättning [Aspose.Words](../../../)


