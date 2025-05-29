---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words per .NET
description: Scopri come l'enum Aspose.Words.PdfCustomPropertiesExport migliora le esportazioni PDF personalizzando le proprietà del documento per ottenere risultati ottimali.
type: docs
weight: 6210
url: /it/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

Specifica il modo[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) vengono esportati in file PDF.

```csharp
public enum PdfCustomPropertiesExport
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Nessuna proprietà personalizzata viene esportata. |
| Standard | `1` | Le proprietà personalizzate vengono esportate come voci nel dizionario /Info. |
| Metadata | `2` | Le proprietà personalizzate sono metadati. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
