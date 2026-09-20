---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry класс"
linktitle: "ChartLegendEntry"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry класс. Представляет запись легенды диаграммы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class


Представляет запись легенды диаграммы. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegendEntry : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                         public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Font](./get_font/)() | Предоставляет доступ к форматированию шрифта этой записи легенды. |
| [get_IsHidden](./get_ishidden/)() const | Получает или задает значение, указывающее, скрыта ли эта запись в легенде диаграммы. Значение по умолчанию — **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden](./get_ishidden/). |
| static [Type](./type/)() |  |
## Примечания


Запись легенды соответствует конкретному ряду диаграммы или линии тренда.

Текст записи является именем ряда или линии тренда. Текст нельзя изменить.

## Примеры



Показывает, как работать со шрифтом легенды.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// Установите размер шрифта по умолчанию для всех записей легенды.
chartLegend->get_Font()->set_Size(14);
// Измените шрифт для конкретной записи легенды.
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// Получите запись легенды для ряда диаграммы.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
