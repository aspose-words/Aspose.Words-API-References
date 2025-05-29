---
title: MailMergeSettings Class
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.MailMergeSettings, um die Dokumentenautomatisierung mit leistungsstarken Serienbrieffunktionen für mehr Effizienz zu optimieren.
type: docs
weight: 6680
url: /de/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Gibt alle Serienbriefinformationen für ein Dokument an.

Um mehr zu erfahren, besuchen Sie die[Serienbriefe und Berichte](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Dokumentationsartikel.

```csharp
public class MailMergeSettings
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [MailMergeSettings](mailmergesettings/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | Gibt den einsbasierten Index des Datensatzes aus der Datenquelle an, der in Microsoft Word angezeigt werden soll. Der Standardwert ist 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | Gibt die Spalte innerhalb der Datenquelle an, die E-Mail-Adressen enthält. Der Standardwert ist eine leere Zeichenfolge. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | Gibt die Art der Fehlerberichterstattung an, die Microsoft Word bei der Serienbrieferstellung durchführen soll. Der Standardwert istDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | Gibt die Verbindungszeichenfolge für die Verbindung mit einer externen Datenquelle an. Der Standardwert ist eine leere Zeichenfolge. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | Gibt den Pfad zur Serienbrief-Datenquelle an. Der Standardwert ist eine leere Zeichenfolge. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | Gibt den Typ der Serienbrief-Datenquelle und die Methode des Datenzugriffs an. Der Standardwert istDefault . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | Gibt an, wie Microsoft Word die Ergebnisse eines Serienbriefs ausgibt. Der Standardwert istDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | Gibt an, wie eine Anwendung, die den Seriendruck ausführt, mit leeren Zeilen in den aus dem Seriendruck resultierenden Dokumenten umgehen soll. Der Standardwert ist`FALSCH` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | Gibt den Pfad zur Quelle des Serienbriefkopfes an. Der Standardwert ist eine leere Zeichenfolge. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | Hier bin ich mir nicht sicher. Die Microsoft Word Automation Reference legt nahe, dass die Abfrage jedes Mal ausgeführt wird, wenn das Dokument in Microsoft Word geöffnet wird. Die OOXML-Spezifikation legt jedoch nahe, dass die Abfrage einen Verweis auf eine externe Abfragedatei enthält, die die eigentliche Abfrage enthält. Der Standardwert ist`FALSCH` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | Gibt an, dass die während eines Seriendruckvorgangs erstellten Dokumente als Anhang und nicht als E-Mail-Text versendet werden sollen. Der Standardwert ist`FALSCH` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | Gibt den Text an, der in der Betreffzeile der während des Serienbriefversands erstellten E-Mails oder Faxe erscheinen soll. Der Standardwert ist eine leere Zeichenfolge. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | Gibt den Hauptdokumenttyp für Serienbriefe an. Der Standardwert istDefault . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | Ruft das Objekt ab oder legt es fest, das die ODSO-Einstellungen (Office Data Source Object) angibt. |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | Enthält die STR-Zeichenfolge (Structured Query Language), die für die angegebene externe Datenquelle ausgeführt werden soll, um den Datensatzsatz zurückzugeben, der beim Ausführen des Seriendruckvorgangs in das Dokument importiert werden soll. Der Standardwert ist eine leere Zeichenfolge. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | Gibt an, dass Microsoft Word die Daten aus der angegebenen externen Datenquelle anzeigen soll, in die Seriendruckfelder eingefügt wurden (z. B. Vorschau zusammengeführter Daten). Der Standardwert ist`FALSCH` . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | Löscht die Serienbriefeinstellungen, sodass beim Speichern des Dokuments keine Serienbriefeinstellungen gespeichert werden und es zu einem normalen Dokument wird. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | Gibt einen tiefen Klon dieses Objekts zurück. |

## Bemerkungen

Sie können dieses Objekt verwenden, um eine Serienbrief-Datenquelle für ein Dokument anzugeben. Diese Informationen (zusammen mit den verfügbaren Datenfeldern) werden in Microsoft Word angezeigt, wenn der Benutzer dieses Dokument öffnet. Oder Sie können dieses Objekt verwenden, um Serienbriefeinstellungen abzufragen, die der Benutzer in Microsoft Word für dieses Dokument angegeben hat.

Normalerweise müssen Sie Objekte dieser Klasse nicht direkt erstellen, da die Seriendruckeinstellungen eines Dokuments immer über die[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) Eigentum.

Um festzustellen, ob es sich bei diesem Dokument um ein Serienbrief-Hauptdokument handelt, überprüfen Sie den Wert der [`MainDocumentType`](./maindocumenttype/) Eigentum.

Um Serienbriefeinstellungen und Datenquelleninformationen aus einem Dokument zu entfernen, können Sie den Befehl verwenden.[`Clear`](./clear/) Methode. Aspose.Words schreibt keine Serienbriefeinstellungen in ein Dokument, wenn die[`MainDocumentType`](./maindocumenttype/) Eigenschaft ist aufNotAMergeDocument oder die[`DataType`](./datatype/) Eigenschaft ist aufNone.

Der beste Weg, die Eigenschaften dieses Objekts zu erlernen, besteht darin, ein Dokument mit einer gewünschten -Datenquelle manuell in Microsoft Word zu erstellen und dieses Dokument dann mit Aspose.Words zu öffnen und die Eigenschaften des[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) Und[`Odso`](./odso/) Objekte. Dies ist ein guter Ansatz, wenn Sie beispielsweise lernen möchten, wie Sie eine Datenquelle programmgesteuert konfigurieren.

Aspose.Words behält Serienbriefinformationen beim Laden, Speichern und Konvertieren von Dokumenten zwischen verschiedenen Formaten bei, verwendet diese Informationen jedoch nicht bei der Durchführung eines eigenen Serienbriefs mit dem[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) Objekt.

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
