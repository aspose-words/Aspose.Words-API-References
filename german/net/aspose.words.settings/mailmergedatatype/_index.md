---
title: MailMergeDataType Enum
linktitle: MailMergeDataType
articleTitle: MailMergeDataType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.MailMergeDataType für die nahtlose Integration externer Datenquellen in Ihre Dokumentautomatisierungsprojekte.
type: docs
weight: 6650
url: /de/net/aspose.words.settings/mailmergedatatype/
---
## MailMergeDataType enumeration

Gibt den Typ einer externen Serienbrief-Datenquelle an.

```csharp
public enum MailMergeDataType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `-1` | Es wurde keine Serienbrief-Datenquelle angegeben. |
| TextFile | `0` | Gibt an, dass ein bestimmtes Dokument über das Dynamic Data Exchange (DDE)-System mit einer Textdatei verbunden wurde. |
| Database | `1` | Gibt an, dass ein bestimmtes Dokument über das Dynamic Data Exchange (DDE)-System mit einer Access-Datenbank verbunden wurde. |
| Spreadsheet | `2` | Gibt an, dass ein bestimmtes Dokument über das Dynamic Data Exchange (DDE)-System mit einer Excel-Tabelle verbunden wurde. |
| Query | `3` | Gibt an, dass ein bestimmtes Dokument mithilfe eines externen Abfragetools mit einer externen Datenquelle verbunden wurde. |
| Odbc | `4` | Gibt an, dass ein bestimmtes Dokument über die Open Database Connectivity-Schnittstelle mit einer externen Datenquelle verbunden wurde. |
| Native | `5` | Gibt an, dass ein bestimmtes Dokument über die Office Data Source Object (ODSO)-Schnittstelle mit einer externen Datenquelle verbunden wurde. |
| Default | `-1` | Ist gleichNone . |

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

* property [DataType](../mailmergesettings/datatype/)
* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
