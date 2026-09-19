---
title: "Aspose::Words::Saving::PdfCustomPropertiesExport enum"
linktitle: "PdfCustomPropertiesExport"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfCustomPropertiesExport enum. Specifica il modo in cui le CustomDocumentProperties vengono esportate in un file PDF in C++."
type: docs
weight: 74000
url: /it/cpp/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enum


Specificare il modo in cui [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) vengono esportate in un file PDF.

```cpp
enum class PdfCustomPropertiesExport
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Nessuna proprietà personalizzata viene esportata. |
| Standard | 1 | Le proprietà personalizzate vengono esportate come voci nel dizionario /Info. Le proprietà personalizzate con i seguenti nomi non vengono esportate: "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped". |
| Metadata | 2 | Le proprietà personalizzate sono Metadati. |

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
