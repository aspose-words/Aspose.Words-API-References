---
title: Enum MailMergeMainDocumentType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.MailMergeMainDocumentType opsomming. Gibt die möglichen Typen für ein SerienbriefQuelldokument an.
type: docs
weight: 5840
url: /de/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

Gibt die möglichen Typen für ein Serienbrief-Quelldokument an.

```csharp
public enum MailMergeMainDocumentType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| NotAMergeDocument | `0` | Dieses Dokument ist kein Seriendruckdokument. |
| FormLetters | `1` | Gibt an, dass das Seriendruck-Quelldokument vom Typ Serienbrief ist. |
| MailingLabels | `2` | Gibt an, dass das Seriendruck-Quelldokument vom Typ „Mailing Label“ ist. |
| Envelopes | `4` | Gibt an, dass das Serienbrief-Quelldokument vom Umschlagtyp ist. |
| Catalog | `8` | Gibt an, dass das Seriendruck-Quelldokument vom Katalogtyp ist. |
| Email | `16` | Gibt an, dass das Seriendruck-Quelldokument vom E-Mail-Nachrichtentyp ist. |
| Fax | `32` | Gibt an, dass das Seriendruck-Quelldokument vom Faxtyp ist. |
| Default | `0` | EntsprichtNotAMergeDocument |

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

* property [MainDocumentType](../mailmergesettings/maindocumenttype/)
* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


