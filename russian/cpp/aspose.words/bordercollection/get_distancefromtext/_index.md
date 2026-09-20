---
title: "Aspose::Words::BorderCollection::get_DistanceFromText method"
linktitle: "get_DistanceFromText"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::BorderCollection::get_DistanceFromText method. Получает или задаёт расстояние границы от текста в пунктах в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/bordercollection/get_distancefromtext/
---
## BorderCollection::get_DistanceFromText method


Получает или задает расстояние границы от текста в пунктах.

```cpp
double Aspose::Words::BorderCollection::get_DistanceFromText()
```

## Примечания


Получает расстояние от текста для первой границы.

Устанавливает расстояние от текста для всех границ в коллекции, исключая диагональные границы.

Не оказывает влияния и будет автоматически сброшено до нуля для границ ячеек таблицы.

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
