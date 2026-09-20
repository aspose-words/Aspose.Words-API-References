---
title: "Aspose::Words::Border::get_DistanceFromText метод"
linktitle: "get_DistanceFromText"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Border::get_DistanceFromText метод. Получает или задает расстояние границы от текста или от края страницы в пунктах в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/border/get_distancefromtext/
---
## Border::get_DistanceFromText method


Получает или задаёт расстояние границы от текста или от края страницы в пунктах.

```cpp
double Aspose::Words::Border::get_DistanceFromText()
```


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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
