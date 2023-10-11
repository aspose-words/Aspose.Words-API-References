---
title: Enum MailMergeDestination
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Settings.MailMergeDestination uppräkning. Anger möjliga resultat som kan genereras när en epostsammanslagning utförs på ett dokument.
type: docs
weight: 5830
url: /sv/net/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enumeration

Anger möjliga resultat som kan genereras när en e-postsammanslagning utförs på ett dokument.

```csharp
public enum MailMergeDestination
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| NewDocument | `0` | Anger att överensstämmande värdapplikationer ska generera nya dokument genom att fylla i fälten i ett givet dokument med data från den angivna externa datakällan. |
| Printer | `1` | Anger att överensstämmande värdapplikationer ska skriva ut de dokument som blir resultatet av att fylla i -fälten i ett givet dokument med externa data från den angivna externa datakällan. |
| Email | `2` | Anger att överensstämmande värdapplikationer ska generera e-postmeddelanden med de dokument som är resultatet av att fyller i fälten i ett givet dokument med data från den angivna externa datakällan. |
| Fax | `4` | Anger att överensstämmande värdapplikationer ska generera fax med hjälp av de dokument som är resultatet av att fyller i fälten i ett givet dokument med data från den angivna externa datakällan. |
| Default | `0` | är lika medNewDocument värde. |

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

* property [Destination](../mailmergesettings/destination/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)


