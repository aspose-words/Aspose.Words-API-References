---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup класс"
linktitle: "ChartSeriesGroup"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup класс. Представляет свойства группы рядов диаграммы, то есть свойства рядов диаграммы одного типа, связанных с одними и теми же осями, в C++."
type: docs
weight: 17334
url: /ru/cpp/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class


Представляет свойства группы серий диаграммы, то есть свойства серий диаграммы одного типа, связанных с одними и теми же осями.

```cpp
class ChartSeriesGroup : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AxisGroup](./get_axisgroup/)() | Получает или задает группу осей, к которой относится эта группа рядов. |
| [get_AxisX](./get_axisx/)() | Обеспечивает доступ к свойствам оси X этой группы рядов. |
| [get_AxisY](./get_axisy/)() | Обеспечивает доступ к свойствам оси Y этой группы рядов. |
| [get_BubbleScale](./get_bubblescale/)() | Получает или задает размер пузырей в процентах от их размера по умолчанию. |
| [get_DoughnutHoleSize](./get_doughnutholesize/)() | Получает или задает размер отверстия родительской кольцевой диаграммы в процентах. |
| [get_FirstSliceAngle](./get_firstsliceangle/)() | Получает или задает угол, в градусах, первого сектора родительской круговой диаграммы. |
| [get_GapWidth](./get_gapwidth/)() | Получает или задает процент ширины промежутка между элементами диаграммы. |
| [get_Overlap](./get_overlap/)() | Получает или задает процент того, насколько перекрываются столбцы или колонки серии. |
| [get_SecondSectionSize](./get_secondsectionsize/)() | Получает или задает размер вторичной секции круговой диаграммы в процентах. |
| [get_Series](./get_series/)() | Получает коллекцию серий, принадлежащих этой группе серий. |
| [get_SeriesType](./get_seriestype/)() | Получает тип серии диаграммы, включенной в эту группу. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisGroup](./set_axisgroup/)(Aspose::Words::Drawing::Charts::AxisGroup) | Сеттер для [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup](./get_axisgroup/). |
| [set_BubbleScale](./set_bubblescale/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale](./get_bubblescale/). |
| [set_DoughnutHoleSize](./set_doughnutholesize/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize](./get_doughnutholesize/). |
| [set_FirstSliceAngle](./set_firstsliceangle/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle](./get_firstsliceangle/). |
| [set_GapWidth](./set_gapwidth/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth](./get_gapwidth/). |
| [set_Overlap](./set_overlap/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap](./get_overlap/). |
| [set_SecondSectionSize](./set_secondsectionsize/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize](./get_secondsectionsize/). |
| static [Type](./type/)() |  |
## Примечания


Комбинированные диаграммы содержат несколько групп серий диаграмм, при этом для каждого типа серии имеется отдельная группа.

Также вы можете создать группу серий диаграммы, чтобы назначить вторичные оси одной или нескольким сериям диаграммы.

Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

## Примеры



Показывает, как работать со вторичной осью диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Удалить автоматически сгенерированную серию.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Создайте дополнительную группу серий, также линейного типа.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Укажите использование вторичных осей для новой группы серий.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// Скрыть вторичную ось X.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// Определить заголовок вторичной оси Y.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Добавьте серию в новую группу серий.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
