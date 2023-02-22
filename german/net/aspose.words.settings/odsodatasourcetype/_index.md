---
title: Enum OdsoDataSourceType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.OdsoDataSourceType opsomming. Gibt den Typ der externen Datenquelle an mit der eine Verbindung hergestellt werden soll als Teil der ODSOVerbindungsinformationen.
type: docs
weight: 5590
url: /de/net/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enumeration

Gibt den Typ der externen Datenquelle an, mit der eine Verbindung hergestellt werden soll, als Teil der ODSO-Verbindungsinformationen.

```csharp
public enum OdsoDataSourceType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Text | `0` | Gibt an, dass ein bestimmtes Dokument mit einer Textdatei verbunden wurde. Möglicherweise wdMergeSubTypeOther. |
| Database | `1` | Gibt an, dass ein bestimmtes Dokument mit einer Datenbank verbunden wurde. Möglicherweise wdMergeSubTypeAccess. |
| AddressBook | `2` | Gibt an, dass ein bestimmtes Dokument mit einem Adressbuch von Kontakten verbunden wurde. Möglicherweise wdMergeSubTypeOAL. |
| Document1 | `3` | Gibt an, dass ein bestimmtes Dokument mit einem anderen Dokumentformat verbunden wurde, das von der produzierenden Anwendung unterstützt wird. Möglicherweise wdMergeSubTypeOLEDBWord. |
| Document2 | `4` | Gibt an, dass ein bestimmtes Dokument mit einem anderen Dokumentformat verbunden wurde, das von der produzierenden Anwendung unterstützt wird. Möglicherweise wdMergeSubTypeWorks. |
| Native | `5` | Gibt an, dass ein bestimmtes Dokument mit einem anderen nativen Dokumentformat der produzierenden Anwendung verbunden wurde. Möglicherweise wdMergeSubTypeOLEDBText |
| Email | `6` | Gibt an, dass ein bestimmtes Dokument mit einer E-Mail-Anwendung verbunden wurde. Möglicherweise wdMergeSubTypeOutlook. |
| None | `7` | Der Typ der externen Datenquelle ist nicht angegeben. Evtl. wdMergeSubTypeWord. |
| Legacy | `8` | Gibt an, dass ein bestimmtes Dokument mit einem Legacy-Dokumentformat verbunden wurde, das von der produzierenden Anwendung unterstützt wird Möglicherweise wdMergeSubTypeWord2000. |
| Master | `9` | Gibt an, dass ein bestimmtes Dokument mit einer Datenquelle verbunden wurde, die andere Datenquellen aggregiert. |
| Default | `7` | EntsprichtNone . |

### Bemerkungen

Die OOXML-Spezifikation ist für diese Aufzählung sehr vage. Ich denke, es könnte der WdMergeSubType -Enumeration http://msdn.microsoft.com/en-us/library/bb237801.aspx entsprechen.

### Beispiele

Zeigt, wie ein Seriendruck mit Daten aus einem Office-Datenquellenobjekt ausgeführt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Erstellen Sie eine Datenquelle in Form einer ASCII-Datei, mit dem "|" Charakter
// fungiert als Trennzeichen, das Spalten trennt. Die erste Zeile enthält die Namen der drei Spalten,
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

// Beim Öffnen dieses Dokuments in Microsoft Word wird der Seriendruck ausgeführt, bevor der Inhalt angezeigt wird. 
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


