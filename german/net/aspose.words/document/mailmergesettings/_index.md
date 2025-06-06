---
title: Document.MailMergeSettings
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Eigenschaft MailMergeSettings alle Serienbriefdaten Ihres Dokuments effizient verwalten und Ihren Arbeitsablauf verbessern können.
type: docs
weight: 280
url: /de/net/aspose.words/document/mailmergesettings/
---
## Document.MailMergeSettings property

Ruft das Objekt ab oder legt es fest, das alle Seriendruckinformationen für ein Dokument enthält.

```csharp
public MailMergeSettings MailMergeSettings { get; set; }
```

## Bemerkungen

Sie können dieses Objekt verwenden, um eine Serienbrief-Datenquelle für ein Dokument anzugeben. Diese Informationen (zusammen mit den verfügbaren Datenfeldern) werden in Microsoft Word angezeigt, wenn der Benutzer dieses Dokument öffnet. Oder Sie können dieses Objekt verwenden, um Serienbriefeinstellungen abzufragen, die der Benutzer in Microsoft Word für dieses Dokument angegeben hat.

Dieses Objekt ist nie`null`.

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

* class [MailMergeSettings](../../../aspose.words.settings/mailmergesettings/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
