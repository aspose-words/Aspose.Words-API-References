---
title: "Aspose::Words::Drawing::Charts::LegendPosition перечисление"
linktitle: "LegendPosition"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::LegendPosition перечисление. Указывает возможные позиции легенды диаграммы в C++."
type: docs
weight: 29000
url: /ru/cpp/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enum


Указывает возможные позиции легенды диаграммы.

```cpp
enum class LegendPosition
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Легенда не будет отображаться для диаграммы. |
| Низ | 1 | Указывает, что легенда будет нарисована в нижней части диаграммы. |
| Слева | 2 | Указывает, что легенда будет нарисована слева от диаграммы. |
| Справа | 3 | Указывает, что легенда будет нарисована справа от диаграммы. |
| Верх | 4 | Указывает, что легенда будет нарисована в верхней части диаграммы. |
| TopRight | 5 | Указывает, что легенда будет нарисована в правом верхнем углу диаграммы. |


## Примеры



Показывает, как изменить внешний вид легенды диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Переместите легенду диаграммы в правый верхний угол.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Освободите место для других элементов диаграммы, таких как график, разрешив им перекрывать легенду.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
