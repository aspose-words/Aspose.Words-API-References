---
title: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor метод"
linktitle: "get_ForeThemeColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor метод. Получает или задает объект ThemeColor, который представляет цвет переднего плана линии в C++."
type: docs
weight: 10334
url: /ru/cpp/aspose.words.drawing/stroke/get_forethemecolor/
---
## Stroke::get_ForeThemeColor method


Получает или задает объект ThemeColor, представляющий цвет переднего плана штриха.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_ForeThemeColor()
```


## Примеры



Показывает, как установить цвет темы переднего плана, а также оттенок и затемнение.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## См. также

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
