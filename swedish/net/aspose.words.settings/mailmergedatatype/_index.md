---
title: Enum MailMergeDataType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Settings.MailMergeDataType uppräkning. Anger typen av en extern kopplingsdatakälla.
type: docs
weight: 5820
url: /sv/net/aspose.words.settings/mailmergedatatype/
---
## MailMergeDataType enumeration

Anger typen av en extern kopplingsdatakälla.

```csharp
public enum MailMergeDataType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `-1` | Ingen kopplingsdatakälla har angetts. |
| TextFile | `0` | Anger att ett visst dokument har kopplats till en textfil via systemet Dynamic Data Exchange (DDE). |
| Database | `1` | Anger att ett visst dokument har kopplats till en Access-databas via systemet Dynamic Data Exchange (DDE). |
| Spreadsheet | `2` | Anger att ett visst dokument har kopplats till ett Excel-kalkylblad via systemet Dynamic Data Exchange (DDE). |
| Query | `3` | Anger att ett givet dokument har kopplats till en extern datakälla med hjälp av ett externt frågeverktyg. |
| Odbc | `4` | Anger att ett givet dokument har kopplats till en extern datakälla via gränssnittet Open Database Connectivity. |
| Native | `5` | Anger att ett givet dokument har kopplats till en extern datakälla via ODSO-gränssnittet (Office Data Source Object). |
| Default | `-1` | MotsvararNone . |

### Exempel

Visar hur man kör en sammankoppling med data från ett Office-datakällobjekt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Skapa en datakälla i form av en ASCII-fil, med "|" karaktär
// fungerar som avgränsaren som separerar kolumner. Den första raden innehåller de tre kolumnernas namn,
// och varje efterföljande rad är en rad med sina respektive värden.
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

 // Att öppna detta dokument i Microsoft Word kommer att köra sammanslagningen innan innehållet visas.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Se även

* property [DataType](../mailmergesettings/datatype/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)


