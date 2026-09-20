---
title: "Aspose::Words::Drawing::Fill::get_BackTintAndShade метод"
linktitle: "get_BackTintAndShade"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Fill::get_BackTintAndShade метод. Получает или задает значение типа double, которое осветляет или затемняет цвет фона в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.drawing/fill/get_backtintandshade/
---
## Fill::get_BackTintAndShade method


Получает или задает значение типа double, которое осветляет или затемняет цвет фона.

```cpp
double Aspose::Words::Drawing::Fill::get_BackTintAndShade()
```

## Примечания


Допустимые значения находятся в диапазоне от -1 (самый темный) до 1 (самый светлый) для этого свойства.

Ноль (0) — нейтральное значение.

## Примеры



Показывает, как задать цвет темы для цвета переднего/заднего плана фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// Примечание: не используйте "BackThemeColor" и "BackTintAndShade" для заливки шрифта.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## См. также

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
