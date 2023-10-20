---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words für .NET
description: PdfSaveOptions CustomPropertiesExport eigendom. Ruft einen Wert ab der den Weg bestimmt oder legt diesen festCustomDocumentProperties werden in eine PDFDatei exportiert in C#.
type: docs
weight: 60
url: /de/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Ruft einen Wert ab, der den Weg bestimmt, oder legt diesen fest[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) werden in eine PDF-Datei exportiert.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## Bemerkungen

Der Standardwert istNone.

Metadata Wert wird beim Speichern in PDF/A. nicht unterstütztStandard wird stattdessen für PDF/A-1 und PDF/A-2 verwendet und None für PDF/A-4.

Standard Wert wird beim Speichern in PDF 2.0. nicht unterstütztMetadata wird stattdessen verwendet.

## Beispiele

Zeigt, wie benutzerdefinierte Eigenschaften beim Konvertieren eines Dokuments in PDF exportiert werden.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „CustomPropertiesExport“ auf „PdfCustomPropertiesExport.None“, um sie zu verwerfen
// benutzerdefinierte Dokumenteigenschaften, während wir das Dokument als .PDF speichern.
// Setzen Sie die Eigenschaft „CustomPropertiesExport“ auf „PdfCustomPropertiesExport.Standard“
// um benutzerdefinierte Eigenschaften im ausgegebenen PDF-Dokument beizubehalten.
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
