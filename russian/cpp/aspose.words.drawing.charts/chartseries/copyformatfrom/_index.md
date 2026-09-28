---
title: "Метод Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom"
linktitle: "CopyFormatFrom"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom. Копирует формат точки данных по умолчанию из точки данных с указанным индексом в C++."
type: docs
weight: 1875
url: /ru/cpp/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries::CopyFormatFrom method


Копирует формат точки данных по умолчанию из точки данных с указанным индексом.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom(int32_t dataPointIndex)
```


## Примеры



Показывает, как скопировать формат точки данных.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

// Получите диаграмму и серию для обновления формата.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_FALSE(dataPoints->HasDefaultFormat(1));

// Скопируйте формат точки данных с индексом 1 в точку данных с индексом 2
// чтобы точка данных 2 выглядела так же, как точка данных 1.
dataPoints->CopyFormat(0, 1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

// Скопировать формат точки данных с индексом 0 в настройки по умолчанию серии, чтобы все точки данных
// в серии, у которой формат по умолчанию выглядит так же, как у точки данных 0.
series->CopyFormatFrom(1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

doc->Save(get_ArtifactsDir() + u"Charts.CopyDataPointFormat.docx");
```

## См. также

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
