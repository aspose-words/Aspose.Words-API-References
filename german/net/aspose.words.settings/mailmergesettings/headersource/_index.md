---
title: MailMergeSettings.HeaderSource
linktitle: HeaderSource
articleTitle: HeaderSource
second_title: Aspose.Words für .NET
description: MailMergeSettings HeaderSource eigendom. Gibt den Pfad zur Quelle des SerienbriefHeaders an. Der Standardwert ist eine leere Zeichenfolge in C#.
type: docs
weight: 100
url: /de/net/aspose.words.settings/mailmergesettings/headersource/
---
## MailMergeSettings.HeaderSource property

Gibt den Pfad zur Quelle des Serienbrief-Headers an. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string HeaderSource { get; set; }
```

## Beispiele

Zeigt, wie eine Datenquelle für einen Serienbrief aus einer Header-Quelle und einer Datenquelle erstellt wird.

```csharp
// Erstellen Sie eine Mailing-Etiketten-Merge-Header-Datei, die aus einer Tabelle mit einer Zeile besteht.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// Erstellen Sie eine Mailing-Etiketten-Zusammenführungsdatendatei, die aus einer Tabelle mit einer Zeile besteht
 // und die gleiche Anzahl von Spalten wie die Tabelle des Header-Dokuments.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// Erstellen Sie ein Zusammenführungszieldokument mit MERGEFIELDS mit Namen wie
// Übereinstimmung mit den Spaltennamen in der Zusammenführungs-Header-Dateitabelle.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// Erstellen Sie eine Datenquelle für unseren Seriendruck, indem Sie zwei Dokumentdateinamen angeben.
// Die Header-Quelle benennt die Spalten der Datenquellentabelle.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// Die Datenquelle stellt Datenzeilen für alle Spalten in der Kopfdokumenttabelle bereit.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// Konfiguriere einen Serienbrief vom Typ „Versandetikett“, der von Microsoft Word ausgeführt wird
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
