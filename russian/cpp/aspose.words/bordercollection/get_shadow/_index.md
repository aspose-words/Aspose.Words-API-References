---
title: "Aspose::Words::BorderCollection::get_Shadow метод"
linktitle: "get_Shadow"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::BorderCollection::get_Shadow метод. Получает или задает значение, указывающее, имеет ли граница тень, в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words/bordercollection/get_shadow/
---
## BorderCollection::get_Shadow method


Получает или задает значение, указывающее, имеет ли граница тень.

```cpp
bool Aspose::Words::BorderCollection::get_Shadow()
```

## Примечания


Получает значение первой границы в коллекции.

Устанавливает значение для всех границ в коллекции, исключая диагональные границы.

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

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
