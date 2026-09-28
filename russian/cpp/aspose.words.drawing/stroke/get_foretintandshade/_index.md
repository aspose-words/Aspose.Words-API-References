---
title: "метод Aspose::Words::Drawing::Stroke::get_ForeTintAndShade"
linktitle: "get_ForeTintAndShade"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Stroke::get_ForeTintAndShade. Получает или задает значение типа double, которое осветляет или затемняет цвет переднего плана штриха в C++."
type: docs
weight: 10667
url: /ru/cpp/aspose.words.drawing/stroke/get_foretintandshade/
---
## Stroke::get_ForeTintAndShade method


Получает или задает значение типа double, которое осветляет или затемняет цвет переднего плана штриха.

```cpp
double Aspose::Words::Drawing::Stroke::get_ForeTintAndShade()
```

## Примечания


Допустимые значения находятся в диапазоне от -1 (самый тёмный) до 1 (самый светлый) для этого свойства. Ноль (0) нейтрален. Попытка установить это свойство в значение меньше -1 или больше 1 приводит к [ArgumentOutOfRangeException](../).

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

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
