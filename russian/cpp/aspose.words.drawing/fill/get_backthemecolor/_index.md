---
title: "Aspose::Words::Drawing::Fill::get_BackThemeColor метод"
linktitle: "get_BackThemeColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Fill::get_BackThemeColor метод. Получает или задает объект ThemeColor, который представляет цвет фона заполнения в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.drawing/fill/get_backthemecolor/
---
## Fill::get_BackThemeColor method


Получает или задает объект ThemeColor, который представляет цвет фона заливки.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Fill::get_BackThemeColor()
```


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

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
