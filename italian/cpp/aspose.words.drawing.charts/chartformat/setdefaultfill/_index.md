---
title: "Aspose::Words::Drawing::Charts::ChartFormat::SetDefaultFill metodo"
linktitle: "SetDefaultFill"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartFormat::SetDefaultFill metodo. Reimposta il riempimento dell'elemento grafico al valore predefinito in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat::SetDefaultFill method


Reimposta il riempimento dell'elemento grafico al valore predefinito.

```cpp
void Aspose::Words::Drawing::Charts::ChartFormat::SetDefaultFill()
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
