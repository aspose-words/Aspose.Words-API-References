---
title: "класс Aspose::Words::Drawing::Charts::ChartAxis"
linktitle: "ChartAxis"
second_title: "Справочник API Aspose.Words для C++"
description: "класс Aspose::Words::Drawing::Charts::ChartAxis. Представляет параметры оси диаграммы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class


Представляет параметры оси диаграммы. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxis : public Aspose::Words::Drawing::Charts::Core::IDmlChartTitleHolder,
                  public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                  public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                  public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AxisBetweenCategories](./get_axisbetweencategories/)() | Получает или задает флаг, указывающий, пересекает ли ось значений ось категорий между категориями. |
| [get_BaseTimeUnit](./get_basetimeunit/)() | Возвращает или задает наименьшую единицу времени, отображаемую на оси временных категорий. |
| [get_CategoryType](./get_categorytype/)() | Получает или задает тип оси категорий. |
| [get_Crosses](./get_crosses/)() | Указывает, как эта ось пересекает перпендикулярную ось. |
| [get_CrossesAt](./get_crossesat/)() | Указывает, где на перпендикулярной оси происходит пересечение оси. |
| [get_DisplayUnit](./get_displayunit/)() | Указывает значение масштабирования единиц отображения для оси значений. |
| [get_Document](./get_document/)() | Возвращает документ, содержащий родительскую диаграмму. |
| [get_Format](./get_format/)() | Обеспечивает доступ к форматированию линий оси и заливке меток делений. |
| [get_HasMajorGridlines](./get_hasmajorgridlines/)() | Получает или задает флаг, указывающий, имеет ли ось основные линии сетки. |
| [get_HasMinorGridlines](./get_hasminorgridlines/)() | Получает или задает флаг, указывающий, имеет ли ось вспомогательные линии сетки. |
| [get_Hidden](./get_hidden/)() | Получает или задает флаг, указывающий, скрыта ли эта ось. |
| [get_MajorTickMark](./get_majortickmark/)() | Возвращает или задает основные деления. |
| [get_MajorUnit](./get_majorunit/)() | Возвращает или задает расстояние между основными делениями. |
| [get_MajorUnitIsAuto](./get_majorunitisauto/)() | Получает или задает флаг, указывающий, следует ли использовать расстояние по умолчанию между основными делениями. |
| [get_MajorUnitScale](./get_majorunitscale/)() | Возвращает или задает значение масштаба для основных делений на оси временных категорий. |
| [get_MinorTickMark](./get_minortickmark/)() | Возвращает или задает вспомогательные деления оси. |
| [get_MinorUnit](./get_minorunit/)() | Возвращает или задает расстояние между вспомогательными делениями. |
| [get_MinorUnitIsAuto](./get_minorunitisauto/)() | Получает или задает флаг, указывающий, следует ли использовать расстояние по умолчанию между вспомогательными делениями. |
| [get_MinorUnitScale](./get_minorunitscale/)() | Возвращает или задает значение масштаба для вспомогательных делений на оси временных категорий. |
| [get_NumberFormat](./get_numberformat/)() | Возвращает объект [ChartNumberFormat](../chartnumberformat/), позволяющий задавать числовые форматы для оси. |
| [get_ReverseOrder](./get_reverseorder/)() | Возвращает или задает флаг, указывающий, должны ли значения оси отображаться в обратном порядке, т.е. от максимального к минимальному. |
| [get_Scaling](./get_scaling/)() | Предоставляет доступ к параметрам масштабирования оси. |
| [get_TickLabels](./get_ticklabels/)() | Предоставляет доступ к свойствам меток делений оси. |
| [get_TickMarkSpacing](./get_tickmarkspacing/)() | Получает или задает интервал, с которым рисуются деления. |
| [get_Title](./get_title/)() | Предоставляет доступ к свойствам заголовка оси. |
| [get_Type](./get_type/)() const | Возвращает тип оси. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisBetweenCategories](./set_axisbetweencategories/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories](./get_axisbetweencategories/). |
| [set_BaseTimeUnit](./set_basetimeunit/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_BaseTimeUnit](./get_basetimeunit/). |
| [set_CategoryType](./set_categorytype/)(Aspose::Words::Drawing::Charts::AxisCategoryType) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_CategoryType](./get_categorytype/). |
| [set_Crosses](./set_crosses/)(Aspose::Words::Drawing::Charts::AxisCrosses) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_Crosses](./get_crosses/). |
| [set_CrossesAt](./set_crossesat/)(double) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt](./get_crossesat/). |
| [set_HasMajorGridlines](./set_hasmajorgridlines/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines](./get_hasmajorgridlines/). |
| [set_HasMinorGridlines](./set_hasminorgridlines/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMinorGridlines](./get_hasminorgridlines/). |
| [set_Hidden](./set_hidden/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden](./get_hidden/). |
| [set_MajorTickMark](./set_majortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorTickMark](./get_majortickmark/). |
| [set_MajorUnit](./set_majorunit/)(double) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnit](./get_majorunit/). |
| [set_MajorUnitIsAuto](./set_majorunitisauto/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitIsAuto](./get_majorunitisauto/). |
| [set_MajorUnitScale](./set_majorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale](./get_majorunitscale/). |
| [set_MinorTickMark](./set_minortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorTickMark](./get_minortickmark/). |
| [set_MinorUnit](./set_minorunit/)(double) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnit](./get_minorunit/). |
| [set_MinorUnitIsAuto](./set_minorunitisauto/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto](./get_minorunitisauto/). |
| [set_MinorUnitScale](./set_minorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale](./get_minorunitscale/). |
| [set_ReverseOrder](./set_reverseorder/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_ReverseOrder](./get_reverseorder/). |
| [set_TickMarkSpacing](./set_tickmarkspacing/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::ChartAxis::get_TickMarkSpacing](./get_tickmarkspacing/). |
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
