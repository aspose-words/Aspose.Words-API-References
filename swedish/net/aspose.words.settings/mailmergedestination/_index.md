---
title: MailMergeDestination Enum
linktitle: MailMergeDestination
articleTitle: MailMergeDestination
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.MailMergeDestination, som definierar resultat för sömlösa dokumentkopplingar. Optimera din dokumenthantering idag!
type: docs
weight: 6660
url: /sv/net/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enumeration

Anger de möjliga resultat som kan genereras när en dokumentkoppling utförs på ett dokument.

```csharp
public enum MailMergeDestination
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| NewDocument | `0` | Anger att kompatibla värdapplikationer ska generera nya dokument genom att fylla i fälten i ett givet dokument med data från den angivna externa datakällan. |
| Printer | `1` | Anger att kompatibla värdprogram ska skriva ut de dokument som är resultatet av att fälten i ett givet dokument fylls i med externa data från den angivna externa datakällan. |
| Email | `2` | Anger att kompatibla webbhotellsapplikationer ska generera e-postmeddelanden med hjälp av de dokument som är resultatet av att fyller i fälten i ett givet dokument med data från den angivna externa datakällan. |
| Fax | `4` | Anger att kompatibla värdapplikationer ska generera fax med hjälp av de dokument som är resultatet av att fyller i fälten i ett givet dokument med data från den angivna externa datakällan. |
| Default | `0` | Är lika medNewDocument värde. |

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

* property [Destination](../mailmergesettings/destination/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
