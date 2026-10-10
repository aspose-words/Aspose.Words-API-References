---
title: "Aspose::Words::FileCorruptedException typedef"
linktitle: "FileCorruptedException"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::FileCorruptedException typedef. Generata durante il caricamento del documento, quando il documento appare corrotto e impossibile da caricare. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 133000
url: /it/cpp/aspose.words/filecorruptedexception/
---
## FileCorruptedException typedef


Generato durante il caricamento del documento, quando il documento sembra corrotto e impossibile da caricare. Per saperne di più, visita l'articolo di documentazione [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
using Aspose::Words::FileCorruptedException = typedef System::ExceptionWrapper<Details_FileCorruptedException>
```


## Esempi



Mostra come intercettare una FileCorruptedException.
```cpp
try
{
    // Se riceviamo un messaggio di errore "Unreadable content" quando tentiamo di aprire un documento con Microsoft Word,
    // probabilmente otterremo un'eccezione generata quando proviamo a caricare quel documento usando Aspose.Words.
    auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted document.docx");
}
catch (Aspose::Words::FileCorruptedException& e)
{
    std::cout << e->get_Message() << std::endl;
}
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
