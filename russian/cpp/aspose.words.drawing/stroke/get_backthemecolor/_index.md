---
title: "Aspose::Words::Drawing::Stroke::get_BackThemeColor метод"
linktitle: "get_BackThemeColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Stroke::get_BackThemeColor метод. Получает или задает объект ThemeColor, который представляет цвет фона штриха в C++."
type: docs
weight: 2167
url: /ru/cpp/aspose.words.drawing/stroke/get_backthemecolor/
---
## Stroke::get_BackThemeColor method


Получает или задаёт объект ThemeColor, представляющий цвет фона обводки.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_BackThemeColor()
```


## Примеры



Показывает, как установить цвет темы фона, а также оттенок и затемнение.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## См. также

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
