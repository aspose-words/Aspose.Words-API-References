---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream metodo"
linktitle: "get_DocumentPartStream"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream metodo. Consente di specificare lo stream in cui la parte del documento verrà salvata in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartstream/
---
## DocumentPartSavingArgs::get_DocumentPartStream method


Consente di specificare lo stream dove verrà salvata la parte del documento.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream() const
```

## Note


Questa proprietà consente di salvare le parti del documento su stream invece che su file durante l'esportazione HTML.

Il valore predefinito è **null**. Quando questa proprietà è **null**, la parte del documento verrà salvata in un file specificato nella proprietà [DocumentPartFileName](../get_documentpartfilename/).

Quando il salvataggio su stream in formato HTML è richiesto da [Save()](../) o [Save()](../) e la prima parte del documento sta per essere salvata, Aspose.Words suggerisce qui lo stream di output principale passato inizialmente dal chiamante.

Quando si salva in formato EPUB, che è un formato contenitore basato su HTML, [DocumentPartStream](./) non può essere specificato perché tutte le parti secondarie saranno incapsulate in un unico pacchetto di output.

## Vedi anche

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
