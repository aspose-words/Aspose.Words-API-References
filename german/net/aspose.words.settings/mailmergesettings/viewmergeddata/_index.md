---
title: MailMergeSettings.ViewMergedData
linktitle: ViewMergedData
articleTitle: ViewMergedData
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ViewMergedData-Eigenschaft von MailMergeSettings in Microsoft Word Ihre Dokumenterstellung durch die Vorschau zusammengeführter Daten aus externen Quellen verbessert.
type: docs
weight: 170
url: /de/net/aspose.words.settings/mailmergesettings/viewmergeddata/
---
## MailMergeSettings.ViewMergedData property

Gibt an, dass Microsoft Word die Daten aus der angegebenen externen Datenquelle anzeigen soll, in die Seriendruckfelder eingefügt wurden (z. B. Vorschau zusammengeführter Daten). Der Standardwert ist`FALSCH` .

```csharp
public bool ViewMergedData { get; set; }
```

## Beispiele

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

// Erstellen Sie eine Datenquelle in Form einer ASCII-Datei, mit dem Zeichen "|"
// dient als Trennzeichen zwischen den Spalten. Die erste Zeile enthält die Namen der drei Spalten,
// und jede nachfolgende Zeile ist eine Reihe mit den jeweiligen Werten.
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

    // Wenn Sie dieses Dokument in Microsoft Word öffnen, wird der Seriendruck ausgeführt, bevor der Inhalt angezeigt wird.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Siehe auch

* class [MailMergeSettings](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
