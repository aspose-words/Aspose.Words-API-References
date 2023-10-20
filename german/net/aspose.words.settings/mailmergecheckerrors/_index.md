---
title: MailMergeCheckErrors Enum
linktitle: MailMergeCheckErrors
articleTitle: MailMergeCheckErrors
second_title: Aspose.Words für .NET
description: Aspose.Words.Settings.MailMergeCheckErrors opsomming. Gibt an wie Microsoft Word beim Seriendruck erkannte Fehler meldet in C#.
type: docs
weight: 5810
url: /de/net/aspose.words.settings/mailmergecheckerrors/
---
## MailMergeCheckErrors enumeration

Gibt an, wie Microsoft Word beim Seriendruck erkannte Fehler meldet.

```csharp
public enum MailMergeCheckErrors
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Simulate | `1` | Simulieren Sie die Zusammenführung und melden Sie Fehler in einem neuen Dokument. |
| PauseOnError | `2` | Schließen Sie die Zusammenführung ab und pausieren Sie, um Fehler zu melden. |
| CollectErrors | `3` | Schließen Sie die Zusammenführung ab und melden Sie Fehler in einem neuen Dokument. |
| Default | `2` | Entspricht demPauseOnError value. |

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

* property [CheckErrors](../mailmergesettings/checkerrors/)
* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
