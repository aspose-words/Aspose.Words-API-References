---
title: "Перечисление Aspose::Words::PageBorderDistanceFrom"
linktitle: "PageBorderDistanceFrom"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::PageBorderDistanceFrom. Указывает расположение границы страницы относительно полей страницы в C++."
type: docs
weight: 107000
url: /ru/cpp/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enum


Указывает позицию границы страницы относительно полей страницы.

```cpp
enum class PageBorderDistanceFrom
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Text | 0 | Позиция [Border](../border/) измеряется от полей страницы. |
| PageEdge | 1 | Позиция [Border](../border/) измеряется от края страницы. |


## Примеры



Показывает, как создать широкую синюю полосу‑границу в верхней части первой страницы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(Aspose::Words::PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
border->set_LineStyle(Aspose::Words::LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
