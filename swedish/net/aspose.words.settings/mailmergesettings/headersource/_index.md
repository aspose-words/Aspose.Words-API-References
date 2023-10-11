---
title: MailMergeSettings.HeaderSource
second_title: Aspose.Words för .NET API Referens
description: MailMergeSettings fast egendom. Anger sökvägen till källan för kopplingshuvudet. Standardvärdet är en tom sträng.
type: docs
weight: 100
url: /sv/net/aspose.words.settings/mailmergesettings/headersource/
---
## MailMergeSettings.HeaderSource property

Anger sökvägen till källan för kopplingshuvudet. Standardvärdet är en tom sträng.

```csharp
public string HeaderSource { get; set; }
```

### Exempel

Visar hur man konstruerar en datakälla för en sammanslagning från en rubrikkälla och en datakälla.

```csharp
// Skapa en sammanslagningshuvudfil för adressetikett, som kommer att bestå av en tabell med en rad.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// Skapa en adressetikettssammanslagningsdatafil som består av en tabell med en rad
 // och samma antal kolumner som rubrikdokumentets tabell.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// Skapa ett sammanslagningsdestinationsdokument med MERGEFIELDS med namn som
// matcha kolumnnamnen i sammanslagningshuvudfiltabellen.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// Konstruera en datakälla för vår sammanslagning genom att ange två dokumentfilnamn.
// Rubrikkällan kommer att namnge kolumnerna i datakälltabellen.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// Datakällan kommer att tillhandahålla rader med data för alla kolumner i rubrikdokumenttabellen.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// Konfigurera en sammanslagning av adressetiketttyp, som Microsoft Word kommer att köra
// så snart vi använder det för att ladda utdatadokumentet.
settings.Query = "SELECT * FROM " + settings.DataSource;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.DataType = MailMergeDataType.TextFile;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.docx");
```

### Se även

* class [MailMergeSettings](../)
* namnutrymme [Aspose.Words.Settings](../../mailmergesettings/)
* hopsättning [Aspose.Words](../../../)


