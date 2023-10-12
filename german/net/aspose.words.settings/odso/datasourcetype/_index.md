---
title: Odso.DataSourceType
second_title: Aspose.Words für .NET-API-Referenz
description: Odso eigendom. Gibt den Typ der externen Datenquelle an mit der eine Verbindung als Teil der ODSOVerbindungsinformationen für diesen Seriendruck hergestellt werden soll. Der Standardwert istDefault .
type: docs
weight: 40
url: /de/net/aspose.words.settings/odso/datasourcetype/
---
## Odso.DataSourceType property

Gibt den Typ der externen Datenquelle an, mit der eine Verbindung als Teil der ODSO-Verbindungsinformationen für diesen Seriendruck hergestellt werden soll. Der Standardwert istDefault .

```csharp
public OdsoDataSourceType DataSourceType { get; set; }
```

### Bemerkungen

Diese Einstellung ist lediglich ein Vorschlag für den Datenquellentyp, der für diesen Serienbrief verwendet wird.

### Beispiele

Zeigt, wie ein Serienbrief mit Daten aus einem Office-Datenquellenobjekt ausgeführt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Erstellen Sie eine Datenquelle in Form einer ASCII-Datei mit dem Zeichen „|“ Charakter
// fungiert als Trennzeichen, das die Spalten trennt. Die erste Zeile enthält die Namen der drei Spalten,
// und jede nachfolgende Zeile ist eine Zeile mit ihren jeweiligen Werten.
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

 // Beim Öffnen dieses Dokuments in Microsoft Word wird der Serienbrief ausgeführt, bevor der Inhalt angezeigt wird.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Siehe auch

* enum [OdsoDataSourceType](../../odsodatasourcetype/)
* class [Odso](../)
* namensraum [Aspose.Words.Settings](../../odso/)
* Montage [Aspose.Words](../../../)


