---
title: "Класс Aspose::Words::Drawing::Charts::Chart"
linktitle: "Диаграмма"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Drawing::Charts::Chart. Предоставляет доступ к свойствам формы диаграммы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.drawing.charts/chart/
---
## Chart class


Предоставляет доступ к свойствам формы диаграммы. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class Chart : public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Axes](./get_axes/)() | Получает коллекцию всех осей этой диаграммы. |
| [get_AxisX](./get_axisx/)() | Обеспечивает доступ к свойствам основной оси X диаграммы. |
| [get_AxisY](./get_axisy/)() | Обеспечивает доступ к свойствам основной оси Y диаграммы. |
| [get_AxisZ](./get_axisz/)() | Обеспечивает доступ к свойствам оси Z диаграммы. |
| [get_DataTable](./get_datatable/)() | Обеспечивает доступ к свойствам таблицы данных этой диаграммы. Таблица данных может быть отображена с помощью свойства [Show](../chartdatatable/get_show/). |
| [get_Format](./get_format/)() | Обеспечивает доступ к форматированию заливки и линий диаграммы. |
| [get_Legend](./get_legend/)() | Обеспечивает доступ к свойствам легенды диаграммы. |
| [get_Series](./get_series/)() | Обеспечивает доступ к коллекции рядов. |
| [get_SeriesGroups](./get_seriesgroups/)() | Обеспечивает доступ к коллекции групп рядов этой диаграммы. |
| [get_SourceFullName](./get_sourcefullname/)() | Получает путь и имя файла xls/xlsx, к которому привязана эта диаграмма. |
| [get_Style](./get_style/)() | Получает стиль диаграммы. |
| [get_Title](./get_title/)() | Обеспечивает доступ к свойствам заголовка диаграммы. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::Charts::Chart::get_SourceFullName](./get_sourcefullname/). |
| [set_Style](./set_style/)(Aspose::Words::Drawing::Charts::ChartStyle) | Устанавливает стиль диаграммы. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как вставить диаграмму и задать заголовок.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте форму диаграммы с помощью DocumentBuilder и получите её диаграмму.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Используйте свойство "Title", чтобы задать нашей диаграмме заголовок, который отображается в верхнем центре области диаграммы.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Установите свойство "Show" в значение "true", чтобы сделать заголовок видимым.
title->set_Show(true);

// Установите свойство "Overlay" в значение "true" Чтобы дать другим элементам диаграммы больше места, позволяя им перекрывать заголовок
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
