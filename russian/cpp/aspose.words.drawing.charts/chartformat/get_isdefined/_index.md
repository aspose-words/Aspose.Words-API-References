---
title: "Метод Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined"
linktitle: "get_IsDefined"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined. Возвращает флаг, указывающий, определён ли какой-либо формат в C++."
type: docs
weight: 2250
url: /ru/cpp/aspose.words.drawing.charts/chartformat/get_isdefined/
---
## ChartFormat::get_IsDefined method


Получает флаг, указывающий, определён ли какой-либо формат.

```cpp
bool Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined()
```


## Примеры



Показывает, как сбросить заливку к значению по умолчанию, определённому в серии.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = series->get_DataPoints()->idx_get(1);

ASSERT_TRUE(dataPoint->get_Format()->get_IsDefined());

dataPoint->get_Format()->SetDefaultFill();

doc->Save(get_ArtifactsDir() + u"Charts.ResetDataPointFill.docx");
```

## См. также

* Class [ChartFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
