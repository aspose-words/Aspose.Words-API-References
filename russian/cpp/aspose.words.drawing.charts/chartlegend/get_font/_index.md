---
title: "Метод Aspose::Words::Drawing::Charts::ChartLegend::get_Font"
linktitle: "get_Font"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::ChartLegend::get_Font. Предоставляет доступ к форматированию шрифта по умолчанию для элементов легенды. Чтобы переопределить форматирование шрифта для конкретного элемента легенды, используйте свойство theFont в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.drawing.charts/chartlegend/get_font/
---
## ChartLegend::get_Font method


Предоставляет доступ к форматированию шрифта по умолчанию для элементов легенды. Чтобы переопределить форматирование шрифта для конкретного элемента легенды, используйте свойство [Font](../../chartlegendentry/get_font/).

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartLegend::get_Font()
```


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

* Class [Font](../../../aspose.words/font/)
* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
