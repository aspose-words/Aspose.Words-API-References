---
title: "Aspose::Words::FileCorruptedException typedef"
linktitle: "FileCorruptedException"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FileCorruptedException typedef. Kastas under dokumentladdning när dokumentet verkar vara korrupt och omöjligt att ladda. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 133000
url: /sv/cpp/aspose.words/filecorruptedexception/
---
## FileCorruptedException typedef


Kastas under dokumentladdning när dokumentet verkar vara korrupt och omöjligt att ladda. För att lära dig mer, besök dokumentationsartikeln [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
using Aspose::Words::FileCorruptedException = typedef System::ExceptionWrapper<Details_FileCorruptedException>
```


## Exempel



Visar hur man fångar ett FileCorruptedException.
```cpp
try
{
    // Om vi får felmeddelandet "Unreadable content" när vi försöker öppna ett dokument med Microsoft Word,
    // så är chansen stor att ett undantag kastas när vi försöker ladda det dokumentet med Aspose.Words.
    auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted document.docx");
}
catch (Aspose::Words::FileCorruptedException& e)
{
    std::cout << e->get_Message() << std::endl;
}
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
