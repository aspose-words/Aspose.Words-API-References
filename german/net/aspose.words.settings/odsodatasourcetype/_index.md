---
title: OdsoDataSourceType Enum
linktitle: OdsoDataSourceType
articleTitle: OdsoDataSourceType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words OdsoDataSourceType-Aufzählung, um einfach eine Verbindung zu externen Datenquellen herzustellen und so Ihre Dokumentverarbeitungsfunktionen zu verbessern.
type: docs
weight: 6720
url: /de/net/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enumeration

Gibt den Typ der externen Datenquelle an, mit der als Teil der ODSO-Verbindungsinformationen eine Verbindung hergestellt werden soll.

```csharp
public enum OdsoDataSourceType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Text | `0` | Gibt an, dass ein bestimmtes Dokument mit einer Textdatei verbunden wurde. Möglicherweise wdMergeSubTypeOther. |
| Database | `1` | Gibt an, dass ein bestimmtes Dokument mit einer Datenbank verbunden wurde. Möglicherweise wdMergeSubTypeAccess. |
| AddressBook | `2` | Gibt an, dass ein bestimmtes Dokument mit einem Adressbuch von Kontakten verknüpft wurde. Möglicherweise wdMergeSubTypeOAL. |
| Document1 | `3` | Gibt an, dass ein bestimmtes Dokument mit einem anderen Dokumentformat verbunden wurde, das von der erstellenden Anwendung unterstützt wird. Möglicherweise wdMergeSubTypeOLEDBWord. |
| Document2 | `4` | Gibt an, dass ein bestimmtes Dokument mit einem anderen Dokumentformat verbunden wurde, das von der erstellenden Anwendung unterstützt wird. Möglicherweise wdMergeSubTypeWorks. |
| Native | `5` | Gibt an, dass ein bestimmtes Dokument mit einem anderen Dokumentformat verbunden wurde, das in der erzeugenden Anwendung nativ ist. Möglicherweise wdMergeSubTypeOLEDBText |
| Email | `6` | Gibt an, dass ein bestimmtes Dokument mit einer E-Mail-Anwendung verbunden wurde. Möglicherweise wdMergeSubTypeOutlook. |
| None | `7` | Der Typ der externen Datenquelle ist nicht angegeben. Möglicherweise wdMergeSubTypeWord. |
| Legacy | `8` | Gibt an, dass ein bestimmtes Dokument mit einem älteren Dokumentformat verbunden wurde, das von der erstellenden Anwendung unterstützt wird. Möglicherweise wdMergeSubTypeWord2000. |
| Master | `9` | Gibt an, dass ein bestimmtes Dokument mit einer Datenquelle verbunden wurde, die andere Datenquellen aggregiert. |
| Default | `7` | Ist gleichNone . |

## Bemerkungen

Die OOXML-Spezifikation ist für diese Enumeration sehr vage. Ich vermute, sie entspricht der Enumeration WdMergeSubType (http://msdn.microsoft.com/en-us/library/bb237801.aspx).

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

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
