---
title: "Metodo Aspose::Words::Saving::PageSavingArgs::get_PageStream"
linktitle: "get_PageStream"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PageSavingArgs::get_PageStream. Consente di specificare il flusso in cui la pagina del documento verrà salvata in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/pagesavingargs/get_pagestream/
---
## PageSavingArgs::get_PageStream method


Consente di specificare lo stream in cui verrà salvata la pagina del documento.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::PageSavingArgs::get_PageStream() const
```

## Note


Questa proprietà consente di salvare le pagine del documento su flussi invece che su file.

Il valore predefinito è **null**. Quando questa proprietà è **null**, la pagina del documento verrà salvata in un file specificato nella proprietà [PageFileName](../get_pagefilename/).

Se sia [PageStream](./) sia [PageFileName](../get_pagefilename/) sono impostati, verrà utilizzato PageStream.

## Vedi anche

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
