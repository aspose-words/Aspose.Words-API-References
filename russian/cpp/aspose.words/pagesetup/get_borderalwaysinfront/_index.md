---
title: "Aspose::Words::PageSetup::get_BorderAlwaysInFront метод"
linktitle: "get_BorderAlwaysInFront"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_BorderAlwaysInFront метод. Указывает, где размещается граница страницы относительно пересекающихся текстов и объектов в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/pagesetup/get_borderalwaysinfront/
---
## PageSetup::get_BorderAlwaysInFront method


Указывает, где граница страницы расположена относительно пересекающихся текстов и объектов.

```cpp
bool Aspose::Words::PageSetup::get_BorderAlwaysInFront()
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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
