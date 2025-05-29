---
title: MailMergeMainDocumentType Enum
linktitle: MailMergeMainDocumentType
articleTitle: MailMergeMainDocumentType
second_title: Aspose.Words för .NET
description: Upptäck enumereringsprogrammet Aspose.Words.MailMergeMainDocumentType, som definierar olika typer av källdokument för dokumentkoppling för sömlös dokumentautomation.
type: docs
weight: 6670
url: /sv/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

Anger möjliga typer för ett källdokument för dokumentkoppling.

```csharp
public enum MailMergeMainDocumentType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| NotAMergeDocument | `0` | Detta dokument är inte ett dokument för koppling av dokument. |
| FormLetters | `1` | Anger att källdokumentet för dokumentkopplingen är av typen standardbrev. |
| MailingLabels | `2` | Anger att källdokumentet för dokumentkopplingen är av typen adressetikett. |
| Envelopes | `4` | Anger att källdokumentet för dokumentkopplingen är av typen kuvert. |
| Catalog | `8` | Anger att källdokumentet för dokumentkopplingen är av katalogtypen. |
| Email | `16` | Anger att källdokumentet för dokumentkopplingen är av typen e-postmeddelande. |
| Fax | `32` | Anger att källdokumentet för dokumentkopplingen är av typen fax. |
| Default | `0` | är lika medNotAMergeDocument |

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

* property [MainDocumentType](../mailmergesettings/maindocumenttype/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
