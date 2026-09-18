---
title: "Aspose::Words::FileCorruptedException typedef"
linktitle: "FileCorruptedException"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FileCorruptedException typedef. Wird beim Laden eines Dokuments ausgelöst, wenn das Dokument beschädigt zu sein scheint und nicht geladen werden kann. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 133000
url: /de/cpp/aspose.words/filecorruptedexception/
---
## FileCorruptedException typedef


Wird beim Laden des Dokuments ausgelöst, wenn das Dokument beschädigt zu sein scheint und nicht geladen werden kann. Weitere Informationen finden Sie im Dokumentationsartikel [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
using Aspose::Words::FileCorruptedException = typedef System::ExceptionWrapper<Details_FileCorruptedException>
```


## Beispiele



Zeigt, wie man eine FileCorruptedException abfängt.
```cpp
try
{
    // If we get an "Unreadable content" error message when trying to open a document using Microsoft Word,
    // besteht die Wahrscheinlichkeit, dass beim Laden dieses Dokuments mit Aspose.Words eine Ausnahme ausgelöst wird.
    auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted document.docx");
}
catch (Aspose::Words::FileCorruptedException& e)
{
    std::cout << e->get_Message() << std::endl;
}
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
