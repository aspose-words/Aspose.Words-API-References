---
title: PdfSaveOptions.ExportDocumentStructure
linktitle: ExportDocumentStructure
articleTitle: ExportDocumentStructure
second_title: Aspose.Words für .NET
description: Steuern Sie die Exportstruktur Ihres Dokuments mit PdfSaveOptions. Verwalten Sie ganz einfach die Einstellungen für eine optimale PDF-Ausgabe und steigern Sie die Effizienz Ihres Workflows.
type: docs
weight: 140
url: /de/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die Dokumentstruktur exportiert werden soll oder nicht.

```csharp
public bool ExportDocumentStructure { get; set; }
```

## Bemerkungen

Dieser Wert wird beim Speichern in PDF/A-1a, PDF/A-2a und PDF/UA-1 ignoriert, da für diese Konformität eine Dokumentstruktur erforderlich ist.

Beachten Sie, dass der Export der Dokumentstruktur den Speicherverbrauch erheblich erhöht, insbesondere bei großen Dokumenten.

## Beispiele

Zeigt, wie Dokumentstrukturelemente erhalten bleiben, was bei der programmgesteuerten Interpretation unseres Dokuments hilfreich sein kann.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();
// Setzen Sie die Eigenschaft "ExportDocumentStructure" auf "true", um die Dokumentstruktur, z. B. Tags, über die
// Navigationsbereich „Inhalt“ von Adobe Acrobat auf Kosten einer größeren Dateigröße.
// Setzen Sie die Eigenschaft „ExportDocumentStructure“ auf „false“, um die Dokumentstruktur nicht zu exportieren.
options.ExportDocumentStructure = exportDocumentStructure;

// Angenommen, wir exportieren die Dokumentstruktur beim Speichern dieses Dokuments. In diesem Fall
// Wir können es mit Adobe Acrobat öffnen und Tags für Elemente wie die Überschrift finden
// und den nächsten Absatz über "Ansicht" -> "Ein-/Ausblenden" -> "Navigationsbereiche" -> "Tags".
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
