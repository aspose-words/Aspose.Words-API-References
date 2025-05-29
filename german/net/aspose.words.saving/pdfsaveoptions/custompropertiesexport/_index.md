---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „PdfSaveOptions CustomPropertiesExport“ Ihre PDF-Exporte verbessert, indem sie CustomDocumentProperties für optimale Ergebnisse steuert.
type: docs
weight: 70
url: /de/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Ruft einen Wert ab oder legt ihn fest, der die Art und Weise bestimmt,[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) werden in eine PDF-Datei exportiert.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## Bemerkungen

Der Standardwert istNone.

Metadata Wert wird beim Speichern im PDF/A-Format nicht unterstützt. Standard wird stattdessen für PDF/A-1 und PDF/A-2 verwendet und None für PDF/A-4.

Standard Wert wird beim Speichern im PDF 2.0-Format nicht unterstützt. Metadata wird stattdessen verwendet.

## Beispiele

Zeigt, wie beim Konvertieren eines Dokuments in PDF benutzerdefinierte Eigenschaften exportiert werden.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „CustomPropertiesExport“ auf „PdfCustomPropertiesExport.None“, um sie zu verwerfen
// benutzerdefinierte Dokumenteigenschaften, wenn wir das Dokument im PDF-Format speichern.
// Setzen Sie die Eigenschaft „CustomPropertiesExport“ auf „PdfCustomPropertiesExport.Standard“
// um benutzerdefinierte Eigenschaften im PDF-Ausgabedokument beizubehalten.
// Setzen Sie die Eigenschaft „CustomPropertiesExport“ auf „PdfCustomPropertiesExport.Metadata“
// um benutzerdefinierte Eigenschaften in einem XMP-Paket beizubehalten.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Siehe auch

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
