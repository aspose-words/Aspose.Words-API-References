---
title: "Метод Aspose::Words::Drawing::Stroke::get_BackTintAndShade"
linktitle: "get_BackTintAndShade"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Stroke::get_BackTintAndShade. Получает или задаёт значение типа double, которое осветляет или затемняет цвет фона обводки в C++."
type: docs
weight: 2334
url: /ru/cpp/aspose.words.drawing/stroke/get_backtintandshade/
---
## Stroke::get_BackTintAndShade method


Получает или задаёт значение типа double, которое осветляет или затемняет цвет фона обводки.

```cpp
double Aspose::Words::Drawing::Stroke::get_BackTintAndShade()
```

## Примечания


Допустимые значения находятся в диапазоне от -1 (самый тёмный) до 1 (самый светлый) для этого свойства. Ноль (0) нейтрален. Попытка установить это свойство в значение меньше -1 или больше 1 приводит к [ArgumentOutOfRangeException](../).

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

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
