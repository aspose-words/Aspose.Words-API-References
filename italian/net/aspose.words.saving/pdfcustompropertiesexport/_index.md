---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words per .NET
description: Aspose.Words.Saving.PdfCustomPropertiesExport enum. Specifica il modoCustomDocumentProperties vengono esportati in un file PDF in C#.
type: docs
weight: 5420
url: /it/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

Specifica il modo[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) vengono esportati in un file PDF.

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

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "CustomPropertiesExport" su "PdfCustomPropertiesExport.None" da eliminare
// proprietà personalizzate del documento mentre salviamo il documento in .PDF.
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
