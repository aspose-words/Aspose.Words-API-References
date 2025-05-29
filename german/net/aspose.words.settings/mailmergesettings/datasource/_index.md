---
title: MailMergeSettings.DataSource
linktitle: DataSource
articleTitle: DataSource
second_title: Aspose.Words für .NET
description: Erfahren Sie, wie Sie die DataSource-Eigenschaft von MailMergeSettings für eine nahtlose Serienbriefintegration festlegen. Geben Sie einfach Ihren Datenquellenpfad an, um optimale Ergebnisse zu erzielen!
type: docs
weight: 60
url: /de/net/aspose.words.settings/mailmergesettings/datasource/
---
## MailMergeSettings.DataSource property

Gibt den Pfad zur Serienbrief-Datenquelle an. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string DataSource { get; set; }
```

## Beispiele

Zeigt, wie aus einer Header-Quelle und einer Datenquelle eine Datenquelle für einen Serienbrief erstellt wird.

```csharp
// Erstellen Sie eine Header-Datei zum Zusammenführen von Adressetiketten, die aus einer Tabelle mit einer Zeile besteht.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// Erstellen Sie eine Seriendruckdatendatei für Adressetiketten, die aus einer Tabelle mit einer Zeile besteht
    // und dieselbe Anzahl von Spalten wie die Tabelle des Kopfdokuments.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// Erstellen Sie ein Zusammenführungszieldokument mit MERGEFIELDS mit Namen, die
// Passen Sie die Spaltennamen in der Tabelle der Zusammenführungsheaderdatei an.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// Erstellen Sie eine Datenquelle für unseren Serienbrief, indem Sie zwei Dokumentdateinamen angeben.
// Die Headerquelle benennt die Spalten der Datenquellentabelle.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// Die Datenquelle stellt Datenzeilen für alle Spalten in der Kopfdokumenttabelle bereit.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// Konfigurieren Sie einen Serienbrief vom Typ „Mailing-Label“, den Microsoft Word ausführt
// sobald wir es zum Laden des Ausgabedokuments verwenden.
settings.Query = "SELECT * FROM " + settings.DataSource;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.DataType = MailMergeDataType.TextFile;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.docx");
```

### Siehe auch

* class [MailMergeSettings](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
