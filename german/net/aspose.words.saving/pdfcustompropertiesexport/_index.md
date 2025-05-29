---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Aufzählung Aspose.Words.PdfCustomPropertiesExport PDF-Exporte verbessert, indem sie Dokumenteigenschaften für optimale Ergebnisse anpasst.
type: docs
weight: 6210
url: /de/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

Gibt die Art und Weise an[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) werden in eine PDF-Datei exportiert.

```csharp
public enum PdfCustomPropertiesExport
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Es werden keine benutzerdefinierten Eigenschaften exportiert. |
| Standard | `1` | Benutzerdefinierte Eigenschaften werden als Einträge in das /Info-Wörterbuch exportiert. |
| Metadata | `2` | Benutzerdefinierte Eigenschaften sind Metadaten. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
