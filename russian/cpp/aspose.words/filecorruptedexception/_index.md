---
title: "Aspose::Words::FileCorruptedException typedef"
linktitle: "FileCorruptedException"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::FileCorruptedException typedef. Выбрасывается при загрузке документа, когда документ кажется повреждённым и его невозможно загрузить. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 133000
url: /ru/cpp/aspose.words/filecorruptedexception/
---
## FileCorruptedException typedef


Выбрасывается при загрузке документа, когда документ кажется повреждённым и его невозможно загрузить. Чтобы узнать больше, посетите статью документации [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
using Aspose::Words::FileCorruptedException = typedef System::ExceptionWrapper<Details_FileCorruptedException>
```


## Примеры



Показывает, как перехватить FileCorruptedException.
```cpp
try
{
    // Если мы получаем сообщение об ошибке "Unreadable content" при попытке открыть документ с помощью Microsoft Word,
    // скорее всего будет выброшено исключение при попытке загрузить этот документ с помощью Aspose.Words.
    auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted document.docx");
}
catch (Aspose::Words::FileCorruptedException& e)
{
    std::cout << e->get_Message() << std::endl;
}
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
