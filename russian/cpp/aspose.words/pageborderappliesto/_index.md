---
title: "Aspose::Words::PageBorderAppliesTo enum"
linktitle: "PageBorderAppliesTo"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageBorderAppliesTo enum. Указывает, на каких страницах печатается граница страницы в C++."
type: docs
weight: 106000
url: /ru/cpp/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enum


Указывает, на каких страницах печатается граница страницы.

```cpp
enum class PageBorderAppliesTo
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| AllPages | 0 | Граница страницы отображается на всех страницах раздела. |
| FirstPage | 1 | Граница страницы отображается только на первой странице раздела. |
| OtherPages | 2 | Граница страницы отображается на всех страницах, кроме первой страницы раздела. |


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
