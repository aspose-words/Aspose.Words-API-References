---
title: "Конструктор Aspose::Words::Saving::PageRange::PageRange"
linktitle: "PageRange"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::Saving::PageRange::PageRange. Создает новый объект диапазона страниц в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.saving/pagerange/pagerange/
---
## PageRange::PageRange constructor


Создаёт новый объект диапазона страниц.

```cpp
Aspose::Words::Saving::PageRange::PageRange(int32_t from, int32_t to)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| from | int32_t | Начальный индекс страницы, начиная с нуля. |
| to | int32_t | Конечный индекс страницы, начиная с нуля. Если он превышает индекс последней страницы в документе, он обрезается, чтобы соответствовать документу при рендеринге. |

## Примеры



Показывает, как извлекать страницы на основе точных диапазонов страниц.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## См. также

* Class [PageRange](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
