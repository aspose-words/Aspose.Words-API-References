---
title: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag"
linktitle: "get_ExportFloatingShapesAsInlineTag"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag. Ottiene o imposta un valore che determina se le forme fluttuanti vengono esportate come tag inline nella struttura del documento in C++."
type: docs
weight: 16500
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_exportfloatingshapesasinlinetag/
---
## PdfSaveOptions::get_ExportFloatingShapesAsInlineTag method


Ottiene o imposta un valore che determina se le forme fluttuanti vengono esportate come tag inline nella struttura del documento.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag() const
```

## Note


Il valore predefinito è **false** e le forme fluttuanti verranno esportate come tag a livello di blocco, posizionati dopo il paragrafo a cui sono ancorate.

Quando il valore è **true**, le forme fluttuanti verranno esportate come tag inline, posizionati all'interno del paragrafo a cui sono ancorate.

Questo valore è ignorato quando [ExportDocumentStructure](../get_exportdocumentstructure/) è **false**.
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
