---
title: MailMergeDataType Enum
linktitle: MailMergeDataType
articleTitle: MailMergeDataType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.MailMergeDataType-enum för sömlös integration av externa datakällor i dina dokumentautomationsprojekt.
type: docs
weight: 6650
url: /sv/net/aspose.words.settings/mailmergedatatype/
---
## MailMergeDataType enumeration

Anger typen av en extern datakälla för dokumentkoppling.

```csharp
public enum MailMergeDataType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `-1` | Ingen datakälla för dokumentkoppling har angetts. |
| TextFile | `0` | Anger att ett givet dokument har kopplats till en textfil via DDE-systemet (Dynamic Data Exchange). |
| Database | `1` | Anger att ett givet dokument har kopplats till en Access-databas via DDE-systemet (Dynamic Data Exchange). |
| Spreadsheet | `2` | Anger att ett givet dokument har kopplats till ett Excel-kalkylblad via DDE-systemet (Dynamic Data Exchange). |
| Query | `3` | Anger att ett givet dokument har kopplats till en extern datakälla med hjälp av ett externt frågeverktyg. |
| Odbc | `4` | Anger att ett givet dokument har anslutits till en extern datakälla via gränssnittet Open Database Connectivity. |
| Native | `5` | Anger att ett givet dokument har anslutits till en extern datakälla via ODSO-gränssnittet (Office Data Source Object). |
| Default | `-1` | är lika medNone . |

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

* property [DataType](../mailmergesettings/datatype/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
