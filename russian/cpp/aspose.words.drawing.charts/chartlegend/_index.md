---
title: "Aspose::Words::Drawing::Charts::ChartLegend class"
linktitle: "ChartLegend"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartLegend class. Представляет свойства легенды диаграммы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class


Представляет свойства легенды диаграммы. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegend : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                    public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Font](./get_font/)() | Обеспечивает доступ к форматированию шрифта по умолчанию для элементов легенды. Чтобы переопределить форматирование шрифта для конкретного элемента легенды, используйте свойство [Font](../chartlegendentry/get_font/). |
| [get_Format](./get_format/)() | Обеспечивает доступ к форматированию заливки и линий легенды. |
| [get_LegendEntries](./get_legendentries/)() const | Возвращает коллекцию элементов легенды для всех серий и трендовых линий родительской диаграммы. |
| [get_Overlay](./get_overlay/)() const | Определяет, разрешено ли другим элементам диаграммы перекрывать легенду. Значение по умолчанию — **false**. |
| [get_Position](./get_position/)() | Указывает положение легенды на диаграмме. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Overlay](./set_overlay/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay](./get_overlay/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::LegendPosition) | Сеттер для [Aspose::Words::Drawing::Charts::ChartLegend::get_Position](./get_position/). |
| static [Type](./type/)() |  |

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
