---
title: "Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined metodo"
linktitle: "get_IsDefined"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined metodo. Ottiene un flag che indica se è definito qualche formato in C++."
type: docs
weight: 2250
url: /it/cpp/aspose.words.drawing.charts/chartformat/get_isdefined/
---
## ChartFormat::get_IsDefined method


Ottiene un flag che indica se è definita qualche formattazione.

```cpp
bool Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined()
```


## Esempi



Mostra come reimpostare il riempimento al valore predefinito definito nella serie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = series->get_DataPoints()->idx_get(1);

ASSERT_TRUE(dataPoint->get_Format()->get_IsDefined());

dataPoint->get_Format()->SetDefaultFill();

doc->Save(get_ArtifactsDir() + u"Charts.ResetDataPointFill.docx");
```

## Vedi anche

* Class [ChartFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
