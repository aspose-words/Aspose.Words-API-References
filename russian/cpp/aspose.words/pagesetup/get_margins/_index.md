---
title: "Метод Aspose::Words::PageSetup::get_Margins"
linktitle: "get_Margins"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PageSetup::get_Margins. Возвращает или задаёт предустановленные Margins страницы в C++."
type: docs
weight: 28000
url: /ru/cpp/aspose.words/pagesetup/get_margins/
---
## PageSetup::get_Margins method


Возвращает или задаёт предустановленные [Margins](../../margins/) страницы.

```cpp
Aspose::Words::Margins Aspose::Words::PageSetup::get_Margins()
```


## Примеры



Показывает, когда необходимо пересчитать макет страниц документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Сохранение документа в PDF, в изображение или печать в первый раз будет автоматически
// кешировать макет документа в его страницах.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Измените документ каким-либо образом.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// В текущей версии Aspose.Words изменение документа не приводит к автоматическому пересозданию
// кешированный макет страницы. Если мы хотим, чтобы кешированный макет
// чтобы оставаться актуальным, нам придётся обновлять его вручную.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## См. также

* Enum [Margins](../../margins/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
