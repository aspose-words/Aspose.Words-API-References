---
title: Aspose::Words::FileCorruptedException typedef
linktitle: FileCorruptedException
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FileCorruptedException typedef. Thrown during document load, when the document appears to be corrupted and impossible to load. To learn more, visit the  documentation article in C++.'
type: docs
weight: 133000
url: /cpp/aspose.words/filecorruptedexception/
---
## FileCorruptedException typedef


Thrown during document load, when the document appears to be corrupted and impossible to load. To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
using Aspose::Words::FileCorruptedException = typedef System::ExceptionWrapper<Details_FileCorruptedException>
```


## Examples



Shows how to catch a FileCorruptedException. 
```cpp
try
{
    // If we get an "Unreadable content" error message when trying to open a document using Microsoft Word,
    // chances are that we will get an exception thrown when trying to load that document using Aspose.Words.
    auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted document.docx");
}
catch (Aspose::Words::FileCorruptedException& e)
{
    std::cout << e->get_Message() << std::endl;
}
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
