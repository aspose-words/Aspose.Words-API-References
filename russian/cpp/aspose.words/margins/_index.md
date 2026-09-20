---
title: "Aspose::Words::Margins enum"
linktitle: "Поля"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Margins enum. Указывает предустановленные поля в C++."
type: docs
weight: 99000
url: /ru/cpp/aspose.words/margins/
---
## Margins enum


Указывает предустановленные поля.

```cpp
enum class Margins
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Обычный | 0 | Обычные поля. |
| Узкие | 1 | Узкие поля. |
| Средние | 2 | Средние поля. |
| Широкие | 3 | Широкие поля. |
| Зеркальные | 4 | Зеркальные поля. |
| Пользовательский | 5 | Пользовательские поля. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
