---
title: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields metodo"
linktitle: "get_PreserveFormFields"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields metodo. Specifica se conservare i campi modulo di Microsoft Word come campi modulo nel PDF o convertirli in testo. Il valore predefinito è false in C++."
type: docs
weight: 28000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_preserveformfields/
---
## PdfSaveOptions::get_PreserveFormFields method


Specifica se conservare i campi modulo di Microsoft Word come campi modulo nel PDF o convertirli in testo. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields() const
```

## Note


I campi modulo di Microsoft Word includono input di testo, menu a discesa e controlli di casella di controllo.

Quando impostato su **false**, questi campi verranno esportati come testo in PDF. Quando impostato su **true**, questi campi verranno esportati come campi modulo PDF.

Durante l'esportazione dei campi modulo in PDF come campi modulo, potrebbe verificarsi una perdita di formattazione perché i campi modulo PDF non supportano tutte le funzionalità dei campi modulo di Microsoft Word.

Inoltre, la dimensione dell'output dipende dalla dimensione del contenuto perché i moduli modificabili in Microsoft Word sono oggetti in linea.
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
