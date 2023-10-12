---
title: Class Odso
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.Odso klas. Gibt die Office Data Source Object ODSOEinstellungen für eine SerienbriefDatenquelle an.
type: docs
weight: 5880
url: /de/net/aspose.words.settings/odso/
---
## Odso class

Gibt die Office Data Source Object (ODSO)-Einstellungen für eine Serienbrief-Datenquelle an.

Um mehr zu erfahren, besuchen Sie die[Serienbrief und Berichterstellung](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Dokumentationsartikel.

```csharp
public class Odso
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Odso](odso/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Gibt das Zeichen an, das als Spaltentrennzeichen interpretiert werden soll, das zum Trennen von Spalten in externen Datenquellen verwendet wird. Der Standardwert ist 0, was bedeutet, dass kein Spaltentrennzeichen definiert ist. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Gibt den Speicherort der externen Datenquelle an, die mit einem Dokument verbunden werden soll, um den Seriendruck durchzuführen. Der Standardwert ist eine leere Zeichenfolge. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Gibt den Typ der externen Datenquelle an, mit der eine Verbindung als Teil der ODSO-Verbindungsinformationen für diesen Seriendruck hergestellt werden soll. Der Standardwert istDefault . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | Ruft eine Sammlung von Objekten ab oder legt diese fest, die angeben, wie Spalten aus der externen Datenquelle den vordefinierten Briefvorlagenfeldnamen im Dokument zugeordnet werden. Dieses Objekt ist niemals vorhanden`Null` . |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Gibt an, dass eine Hostinganwendung die erste Datenzeile in der angegebenen externen Datenquelle als Kopfzeile behandeln soll, die die Namen jeder Spalte in der Datenquelle enthält. Der Standardwert ist`FALSCH` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Ruft eine Sammlung von Objekten ab oder legt diese fest, die den Einschluss/Ausschluss einzelner Datensätze in den Seriendruck festlegen. Dieses Objekt ist niemals vorhanden`Null` . |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Gibt den bestimmten Datensatz an, mit dem eine Quelle innerhalb einer externen Datenquelle verbunden werden soll. Der Standardwert ist eine leere Zeichenfolge. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Gibt die UDL-Verbindungszeichenfolge (Universal Data Link) an, die zum Herstellen einer Verbindung mit einer externen Datenquelle verwendet wird. Der Standardwert ist eine leere Zeichenfolge. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Gibt einen tiefen Klon dieses Objekts zurück. |

### Bemerkungen

ODSO scheint die „neue“ Methode zu sein, die die neueren Microsoft Word-Versionen bevorzugen, wenn sie bestimmte -Typen von Datenquellen für ein Seriendruckdokument angeben. ODSO erschien wahrscheinlich erstmals in Microsoft Word 2000.

Die Verwendung von ODSO ist schlecht dokumentiert und der beste Weg, um zu lernen, wie man die Eigenschaften dieses Objekts verwendet, besteht darin, manuell in Microsoft Word ein Dokument mit einer gewünschten Datenquelle zu erstellen und dieses Dokument dann mit Aspose.Words zu öffnen und die Eigenschaften zu untersuchen des[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) und [`Odso`](../mailmergesettings/odso/)Objekte. Dies ist ein guter Ansatz, wenn Sie beispielsweise lernen möchten, wie Sie programmgesteuert eine Datenquelle konfigurieren.

Normalerweise müssen Sie Objekte dieser Klasse nicht direkt erstellen, da ODSO-Einstellungen immer über verfügbar sind[`Odso`](../mailmergesettings/odso/) Eigentum.

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

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


