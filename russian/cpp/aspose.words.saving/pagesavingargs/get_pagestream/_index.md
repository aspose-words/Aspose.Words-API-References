---
title: "Метод Aspose::Words::Saving::PageSavingArgs::get_PageStream"
linktitle: "get_PageStream"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::PageSavingArgs::get_PageStream. Позволяет указать поток, в который будет сохраняться страница документа в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/pagesavingargs/get_pagestream/
---
## PageSavingArgs::get_PageStream method


Позволяет указать поток, в который будет сохранена страница документа.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::PageSavingArgs::get_PageStream() const
```

## Примечания


Это свойство позволяет сохранять страницы документа в потоки вместо файлов.

Значение по умолчанию — **null**. Когда это свойство равно **null**, страница документа будет сохраняться в файл, указанный в свойстве [PageFileName](../get_pagefilename/).

Если заданы как [PageStream](./), так и [PageFileName](../get_pagefilename/), будет использован PageStream.

## См. также

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
