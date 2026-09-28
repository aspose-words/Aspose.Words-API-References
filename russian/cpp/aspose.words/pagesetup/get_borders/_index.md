---
title: "Aspose::Words::PageSetup::get_Borders метод"
linktitle: "get_Borders"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_Borders метод. Получает коллекцию границ страницы в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/pagesetup/get_borders/
---
## PageSetup::get_Borders method


Получает коллекцию границ страницы.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::PageSetup::get_Borders()
```


## Примеры



Показывает, как создать зеленую волнистую границу страницы с тенью.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorders.docx");
```

## См. также

* Class [BorderCollection](../../bordercollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
