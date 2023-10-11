---
title: Enum MailMergeMainDocumentType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Settings.MailMergeMainDocumentType uppräkning. Anger de möjliga typerna för ett källdokument för kopplingsdokument.
type: docs
weight: 5840
url: /sv/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

Anger de möjliga typerna för ett källdokument för kopplingsdokument.

```csharp
public enum MailMergeMainDocumentType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| NotAMergeDocument | `0` | Det här dokumentet är inte ett kopplingsdokument. |
| FormLetters | `1` | Anger att källdokumentet för e-postsammanslagning är av typen standardbrev. |
| MailingLabels | `2` | Anger att källdokumentet för sammanslagningen är av adressetiketttypen. |
| Envelopes | `4` | Anger att källdokumentet för sammanslagningen är av kuverttypen. |
| Catalog | `8` | Anger att källdokumentet för sammanslagningen är av katalogtypen. |
| Email | `16` | Anger att källdokumentet för e-postsammanslagning är av typen e-postmeddelande. |
| Fax | `32` | Anger att källdokumentet för sammanslagningen är av faxtypen. |
| Default | `0` | MotsvararNotAMergeDocument |

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

* property [MainDocumentType](../mailmergesettings/maindocumenttype/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)


