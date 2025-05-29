---
title: Document.MailMergeSettings
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen MailMergeSettings för att hantera alla dina dokuments kopplingsdata effektivt och förbättra ditt arbetsflöde.
type: docs
weight: 280
url: /sv/net/aspose.words/document/mailmergesettings/
---
## Document.MailMergeSettings property

Hämtar eller anger objektet som innehåller all information om dokumentkoppling för ett dokument.

```csharp
public MailMergeSettings MailMergeSettings { get; set; }
```

## Anmärkningar

Du kan använda det här objektet för att ange en datakälla för kopplad dokument för ett dokument och denna information (tillsammans med tillgängliga datafält) visas i Microsoft Word när användaren öppnar dokumentet. Eller så kan du använda det här objektet för att fråga efter inställningar för kopplad dokument som användaren har angett i Microsoft Word för det här dokumentet.

Detta objekt är aldrig`null`.

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

* class [MailMergeSettings](../../../aspose.words.settings/mailmergesettings/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
