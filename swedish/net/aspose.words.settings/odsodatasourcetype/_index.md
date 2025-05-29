---
title: OdsoDataSourceType Enum
linktitle: OdsoDataSourceType
articleTitle: OdsoDataSourceType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words OdsoDataSourceType-enum för att enkelt ansluta till externa datakällor och förbättra dina dokumentbehandlingsmöjligheter.
type: docs
weight: 6720
url: /sv/net/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enumeration

Anger typen av extern datakälla som ska anslutas till som en del av ODSO-anslutningsinformationen.

```csharp
public enum OdsoDataSourceType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Text | `0` | Anger att ett givet dokument har kopplats till en textfil. Möjligen wdMergeSubTypeOther. |
| Database | `1` | Anger att ett givet dokument har kopplats till en databas. Möjligen wdMergeSubTypeAccess. |
| AddressBook | `2` | Anger att ett givet dokument har kopplats till en adressbok med kontakter. Möjligen wdMergeSubTypeOAL. |
| Document1 | `3` | Anger att ett givet dokument har kopplats till ett annat dokumentformat som stöds av det producerande programmet. Möjligen wdMergeSubTypeOLEDBWord. |
| Document2 | `4` | Anger att ett givet dokument har kopplats till ett annat dokumentformat som stöds av det producerande programmet. Möjligen wdMergeSubTypeWorks. |
| Native | `5` | Anger att ett givet dokument har kopplats till ett annat dokumentformat som är ursprungligt för den producerande applikationen. Möjligen wdMergeSubTypeOLEDBText |
| Email | `6` | Anger att ett givet dokument har kopplats till ett e-postprogram. Möjligen wdMergeSubTypeOutlook. |
| None | `7` | Typen för den externa datakällan är inte specificerad. Möjligen wdMergeSubTypeWord. |
| Legacy | `8` | Anger att ett givet dokument har kopplats till ett äldre dokumentformat som stöds av det producerande programmet. Möjligen wdMergeSubTypeWord2000. |
| Master | `9` | Anger att ett givet dokument har kopplats till en datakälla som aggregerar andra datakällor. |
| Default | `7` | är lika medNone . |

## Anmärkningar

OOXML-specifikationen är väldigt vag för denna uppräkning. Jag antar att den kan motsvara WdMergeSubType -uppräkningen http://msdn.microsoft.com/en-us/library/bb237801.aspx.

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

* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
