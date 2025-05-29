---
title: MailMergeSettings.Destination
linktitle: Destination
articleTitle: Destination
second_title: Aspose.Words för .NET
description: Upptäck hur du anpassar egenskapen MailMergeSettings Destination i Microsoft Word för skräddarsydda dokumentkopplingsresultat. Maximera din dokumenteffektivitet idag!
type: docs
weight: 80
url: /sv/net/aspose.words.settings/mailmergesettings/destination/
---
## MailMergeSettings.Destination property

Anger hur Microsoft Word ska skriva ut resultatet av en dokumentkoppling. Standardvärdet ärDefault .

```csharp
public MailMergeDestination Destination { get; set; }
```

## Exempel

Visar hur man utför en dokumentkoppling med data från ett Office-datakällobjekt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Skapa en datakälla i form av en ASCII-fil, med tecknet "|"
// fungerar som avgränsare som separerar kolumner. Den första raden innehåller namnen på de tre kolumnerna,
// och varje efterföljande rad är en rad med deras respektive värden.
string[] lines = { "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = ArtifactsDir + "MailMerge.MailMergeSettings.DataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

MailMergeSettings settings = doc.MailMergeSettings;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.CheckErrors = MailMergeCheckErrors.Simulate;
settings.DataType = MailMergeDataType.Native;
settings.DataSource = dataSrcFilename;
settings.Query = "SELECT * FROM " + doc.MailMergeSettings.DataSource;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

Assert.AreEqual(MailMergeDestination.Default, settings.Destination);
Assert.False(settings.DoNotSupressBlankLines);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.Clone());
Assert.AreNotSame(settings, settings.Clone());

 // Om du öppnar det här dokumentet i Microsoft Word körs dokumentkopplingen innan innehållet visas.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Se även

* enum [MailMergeDestination](../../mailmergedestination/)
* class [MailMergeSettings](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
