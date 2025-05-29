---
title: FieldBibliography.FilterLanguageId
linktitle: FilterLanguageId
articleTitle: FilterLanguageId
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen FieldBibliography FilterLanguageId förbättrar din hantering av bibliografiska data genom att filtrera källor efter språk för exakta resultat.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldbibliography/filterlanguageid/
---
## FieldBibliography.FilterLanguageId property

Hämtar eller ställer in språk-ID:t som används för att filtrera bibliografiska data till endast de källor i dokumentet som använder det språket.

```csharp
public string FilterLanguageId { get; set; }
```

## Exempel

Visar hur man arbetar med fälten CITATION och BIBLIOGRAFI.

```csharp
// Öppna ett dokument som innehåller bibliografiska källor som vi kan hitta i
// Microsoft Word via referenser -> Citat och bibliografi -> Hantera källor.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Skapa en hänvisning med bara sidnumret och författaren till den refererade boken.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Vi hänvisar till källor med hjälp av deras taggnamn.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Skapa en mer detaljerad hänvisning som citerar två källor.
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

// Vi kan använda ett fält för BIBLIOGRAFI för att visa alla källor i dokumentet.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Se även

* class [FieldBibliography](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
