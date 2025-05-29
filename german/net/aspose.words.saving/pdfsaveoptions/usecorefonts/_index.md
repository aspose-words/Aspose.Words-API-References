---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre PDFs mit PdfSaveOptions! Steuern Sie die Schriftartenersetzung für TrueType-Schriftarten wie Arial und Times New Roman, um die Dokumentqualität zu verbessern.
type: docs
weight: 330
url: /de/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob die TrueType-Schriftarten Arial, Times New Roman, Courier New und Symbol durch PDF Type 1-Kernschriftarten ersetzt werden sollen oder nicht.

```csharp
public bool UseCoreFonts { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` Wenn dieser Wert auf`WAHR` Die Schriftarten Arial, Times New Roman, Courier New und Symbol werden im PDF-Dokument durch die entsprechende Kernschriftart Type 1 ersetzt.

Die wichtigsten PDF-Schriftarten bzw. deren Schriftmetriken und geeignete Ersatzschriftarten müssen für jede PDF-Viewer-Anwendung verfügbar sein.

Diese Einstellung funktioniert nur für Text in ANSI-Kodierung (Windows-1252). Nicht-ANSI-Text wird unabhängig von dieser Einstellung mit eingebetteter TrueType-Schriftart geschrieben.

Die PDF/A- und PDF/UA-Konformität erfordert die Einbettung aller Schriftarten.`FALSCH` Beim Speichern im PDF/A- und PDF/UA-Format wird automatisch der Wert verwendet.

Beim Speichern im PDF 2.0-Format werden Kernschriftarten nicht unterstützt.`FALSCH` Beim Speichern im PDF 2.0-Format wird automatisch der Wert verwendet.

Diese Option hat eine höhere Priorität als[`FontEmbeddingMode`](../fontembeddingmode/) Option.

## Beispiele

Zeigt, wie die Schriftartenersetzung für PDF Type 1 aktiviert/deaktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();
// Setzen Sie die Eigenschaft „UseCoreFonts“ auf „true“, um einige Schriftarten zu ersetzen,
// Einschließen der beiden Schriftarten in unser Dokument mit ihren PDF Type 1-Äquivalenten.
// Setzen Sie die Eigenschaft „UseCoreFonts“ auf „false“, um PDF Type 1-Schriftarten nicht anzuwenden.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
