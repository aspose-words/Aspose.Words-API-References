---
title: "Aspose::Words::Drawing::Charts::AxisTickLabels class"
linktitle: "AxisTickLabels"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::AxisTickLabels class. Представляет свойства меток делений оси в C++."
type: docs
weight: 3250
url: /ru/cpp/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class


Представляет свойства меток делений оси.

```cpp
class AxisTickLabels : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Получает или задает выравнивание текста меток делений оси. |
| [get_Font](./get_font/)() | Обеспечивает доступ к форматированию шрифта меток делений. |
| [get_IsAutoSpacing](./get_isautospacing/)() | Получает или задает флаг, указывающий, использовать ли автоматический интервал при отрисовке меток делений. |
| [get_Offset](./get_offset/)() | Получает или задает расстояние меток делений от оси. |
| [get_Orientation](./get_orientation/)() | Получает или задает ориентацию текста меток делений. |
| [get_Position](./get_position/)() | Получает или задает позицию меток делений на оси. |
| [get_Rotation](./get_rotation/)() | Получает или задает вращение меток делений в градусах. |
| [get_Spacing](./get_spacing/)() | Получает или задает интервал, с которым рисуются подписи делений. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Сеттер для [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Alignment](./get_alignment/). |
| [set_IsAutoSpacing](./set_isautospacing/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::AxisTickLabels::get_IsAutoSpacing](./get_isautospacing/). |
| [set_Offset](./set_offset/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Offset](./get_offset/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Сеттер для [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::AxisTickLabelPosition) | Сеттер для [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation](./get_rotation/). |
| [set_Spacing](./set_spacing/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Spacing](./get_spacing/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как вставить диаграмму и изменить внешний вид её осей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Очистите демонстрационную серию данных диаграммы, чтобы начать с чистой диаграммы.
chart->get_Series()->Clear();

// Вставьте серию диаграммы с категориями для оси X и соответствующими числовыми значениями для оси Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// У осей диаграммы есть различные параметры, которые могут изменить их внешний вид,
// например, их направление, основные/второстепенные деления и метки.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Category);
xAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

ASPOSE_ASSERT_EQ(doc, xAxis->get_Document());

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Automatic);
yAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
yAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::NextToAxis);
yAxis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
yAxis->get_TickLabels()->get_Font()->set_Color(System::Drawing::Color::get_Red());
yAxis->get_TickLabels()->set_Spacing(1);

// У столбчатых диаграмм нет оси Z.
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
