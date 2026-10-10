---
title: "Metodo Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen"
linktitle: "get_KeepDocumentPartStreamOpen"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen. Specifica se Aspose.Words deve mantenere il flusso aperto o chiuderlo dopo aver salvato una parte del documento in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/documentpartsavingargs/get_keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen method


Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo aver salvato una parte del documento.

```cpp
bool Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen() const
```

## Note


Il valore predefinito è **false** e Aspose.Words chiuderà il flusso fornito nella proprietà [DocumentPartStream](../get_documentpartstream/) dopo aver scritto una parte del documento al suo interno. Specificare **true** per mantenere il flusso aperto. Si noti che il flusso di output principale fornito nella chiamata a [Save()](../) o [Save()](../) non verrà mai chiuso da Aspose.Words anche se [KeepDocumentPartStreamOpen](./) è impostato su **false**.

## Vedi anche

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
