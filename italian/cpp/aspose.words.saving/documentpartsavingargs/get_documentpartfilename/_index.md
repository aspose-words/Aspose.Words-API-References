---
title: "Metodo Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName"
linktitle: "get_DocumentPartFileName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName. Ottiene o imposta il nome file (senza percorso) in cui la parte del documento verrà salvata in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartfilename/
---
## DocumentPartSavingArgs::get_DocumentPartFileName method


Ottiene o imposta il nome file (senza percorso) dove verrà salvata la parte del documento.

```cpp
System::String Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName() const
```

## Note


Questa proprietà consente di ridefinire come vengono generati i nomi file delle parti del documento durante l'esportazione in HTML o EPUB.

Quando il callback viene invocato, questa proprietà contiene il nome file generato da Aspose.Words. È possibile modificare il valore di questa proprietà per salvare la parte del documento in un file diverso. Si noti che il nome file per ogni parte deve essere univoco.

[DocumentPartFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

## Vedi anche

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
