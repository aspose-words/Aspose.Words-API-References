---
title: Enum MailMergeCheckErrors
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Settings.MailMergeCheckErrors uppräkning. Anger hur Microsoft Word kommer att rapportera fel som upptäcks under sammanslagningen.
type: docs
weight: 5810
url: /sv/net/aspose.words.settings/mailmergecheckerrors/
---
## MailMergeCheckErrors enumeration

Anger hur Microsoft Word kommer att rapportera fel som upptäcks under sammanslagningen.

```csharp
public enum MailMergeCheckErrors
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Simulate | `1` | Simulera sammanslagningen och rapportera fel i ett nytt dokument. |
| PauseOnError | `2` | Slutför sammanslagningen och pausa för att rapportera fel. |
| CollectErrors | `3` | Slutför sammanslagningen och rapportera fel i ett nytt dokument. |
| Default | `2` | är lika medPauseOnError värde. |

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

* property [CheckErrors](../mailmergesettings/checkerrors/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)


