---
title: MailMergeSettings.HeaderSource
linktitle: HeaderSource
articleTitle: HeaderSource
second_title: Aspose.Words för .NET
description: Upptäck egenskapen MailMergeSettings HeaderSource, definiera enkelt din sökväg för dokumentkopplingsrubriken. Optimera ditt dokumentarbetsflöde idag!
type: docs
weight: 100
url: /sv/net/aspose.words.settings/mailmergesettings/headersource/
---
## MailMergeSettings.HeaderSource property

Anger sökvägen till källan för headern för koppling av dokument. Standardvärdet är en tom sträng.

```csharp
public string HeaderSource { get; set; }
```

## Exempel

Visar hur man konstruerar en datakälla för en dokumentkoppling från en rubrikkälla och en datakälla.

```csharp
// Skapa en headerfil för sammanslagning av adressetiketter, som kommer att bestå av en tabell med en rad.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// Skapa en datafil för sammanslagning av adressetiketter som består av en tabell med en rad
 // och samma antal kolumner som headerdokumentets tabell.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// Skapa ett sammanslagningsdokument med MERGEFIELDS med namn som
// matcha kolumnnamnen i tabellen för merge header-filen.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// Skapa en datakälla för vår dokumentkoppling genom att ange två dokumentfilnamn.
// Rubrikkällan namnger kolumnerna i datakällstabellen.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// Datakällan kommer att tillhandahålla datarader för alla kolumner i huvuddokumenttabellen.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// Konfigurera en koppling av adressetiketter, som Microsoft Word kommer att köra
// så snart vi använder den för att ladda utdatadokumentet.
settings.Query = "SELECT * FROM " + settings.DataSource;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.DataType = MailMergeDataType.TextFile;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.docx");
```

### Se även

* class [MailMergeSettings](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
