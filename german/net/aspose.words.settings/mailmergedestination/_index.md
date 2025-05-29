---
title: MailMergeDestination Enum
linktitle: MailMergeDestination
articleTitle: MailMergeDestination
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.MailMergeDestination, die Ergebnisse für nahtlose Serienbriefe definiert. Optimieren Sie Ihre Dokumentenverarbeitung noch heute!
type: docs
weight: 6660
url: /de/net/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enumeration

Gibt die möglichen Ergebnisse an, die generiert werden können, wenn ein Serienbrief für ein Dokument ausgeführt wird.

```csharp
public enum MailMergeDestination
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| NewDocument | `0` | Gibt an, dass konforme Hosting-Anwendungen neue Dokumente generieren sollen, indem sie die Felder innerhalb eines bestimmten Dokuments mit Daten aus der angegebenen externen Datenquelle füllen. |
| Printer | `1` | Gibt an, dass konforme Hosting-Anwendungen die Dokumente drucken sollen, die sich aus dem Auffüllen der -Felder innerhalb eines bestimmten Dokuments mit externen Daten aus der angegebenen externen Datenquelle ergeben. |
| Email | `2` | Gibt an, dass konforme Hosting-Anwendungen E-Mails unter Verwendung der Dokumente generieren sollen, die sich aus dem Auffüllen der Felder in einem bestimmten Dokument mit Daten aus der angegebenen externen Datenquelle ergeben. |
| Fax | `4` | Gibt an, dass konforme Hosting-Anwendungen Faxe mithilfe der Dokumente generieren sollen, die sich aus dem Auffüllen der Felder in einem bestimmten Dokument mit Daten aus der angegebenen externen Datenquelle ergeben. |
| Default | `0` | Entspricht demNewDocument Wert. |

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

* property [Destination](../mailmergesettings/destination/)
* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
