---
title: "Перечисление Aspose::Words::Drawing::Charts::ChartStyle"
linktitle: "ChartStyle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartStyle enum. Указывает предопределённые стили диаграммы в C++."
type: docs
weight: 27875
url: /ru/cpp/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enum


Указывает предопределённые стили диаграммы.

```cpp
enum class ChartStyle
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Обычный | 0 | Представляет стиль диаграммы по умолчанию. |
| Muted | 1 | Стиль с приглушёнными цветами. |
| Saturated | 2 | Стиль с более насыщенными цветами. |
| Shaded | 3 | Стиль с затенёнными точками данных. |
| Flat | 4 | Стиль с плоскими точками данных без градиента. |
| Shadowed | 5 | Стиль с точками данных, имеющими тень. |
| Градиент | 6 | Стиль с градиентной заливкой точек данных. |
| Original | 7 | Стиль с оригинальным внешним видом диаграммы. |
| Transparent1 | 8 | Стиль с прозрачными точками данных. |
| Transparent2 | 9 | Стиль с прозрачными точками данных. |
| Outline | 10 | Стиль с точками данных без заливки, только с контуром. |
| OutlineBlack | 11 | Стиль с чёрным фоном диаграммы, где точки данных без заливки, только с контуром. |
| Черный | 12 | Стиль с чёрным фоном диаграммы. |
| Grey | 13 | Стиль с серым градиентным фоном диаграммы. |
| Синий | 14 | Стиль с синим фоном диаграммы. |
| ShadedPlot | 15 | Стиль, в котором область построения затенена. |


## Примеры



Показывает, как установить и получить стиль диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте диаграмму в стиле Black.
builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 250, Aspose::Words::Drawing::Charts::ChartStyle::Black);

doc->Save(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

// Получить диаграмму для обновления.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Получить стиль диаграммы.
ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartStyle::Black, chart->get_Style());
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
