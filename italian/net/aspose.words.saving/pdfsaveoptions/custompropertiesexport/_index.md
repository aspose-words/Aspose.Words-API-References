---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words per .NET
description: Scopri come la proprietà CustomPropertiesExport di PdfSaveOptions migliora le tue esportazioni PDF controllando CustomDocumentProperties per risultati ottimali.
type: docs
weight: 70
url: /it/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Ottiene o imposta un valore che determina il modo in cui[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) vengono esportati in file PDF.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## Osservazioni

Il valore predefinito èNone.

Metadata il valore non è supportato durante il salvataggio in PDF/A. Standard verrà utilizzato invece per PDF/A-1 e PDF/A-2 e None per PDF/A-4.

Standard il valore non è supportato durante il salvataggio in PDF 2.0. Metadata verrà utilizzato al suo posto.

## Esempi

Mostra come esportare proprietà personalizzate durante la conversione di un documento in PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "CustomPropertiesExport" su "PdfCustomPropertiesExport.None" per scartarla
// proprietà personalizzate del documento quando salviamo il documento in formato .PDF.
// Imposta la proprietà "CustomPropertiesExport" su "PdfCustomPropertiesExport.Standard"
// per preservare le proprietà personalizzate all'interno del documento PDF di output.
// Imposta la proprietà "CustomPropertiesExport" su "PdfCustomPropertiesExport.Metadata"
// per preservare le proprietà personalizzate in un pacchetto XMP.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Guarda anche

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
