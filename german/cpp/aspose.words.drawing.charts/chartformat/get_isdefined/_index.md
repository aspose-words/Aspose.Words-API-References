---
title: "Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined Methode"
linktitle: "get_IsDefined"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined Methode. Gibt ein Flag zurück, das angibt, ob ein Format in C++ definiert ist."
type: docs
weight: 2250
url: /de/cpp/aspose.words.drawing.charts/chartformat/get_isdefined/
---
## ChartFormat::get_IsDefined method


Liefert ein Flag, das angibt, ob ein Format definiert ist.

```cpp
bool Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined()
```


## Beispiele



Zeigt, wie man die Füllung auf den in der Serie definierten Standardwert zurücksetzt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = series->get_DataPoints()->idx_get(1);

ASSERT_TRUE(dataPoint->get_Format()->get_IsDefined());

dataPoint->get_Format()->SetDefaultFill();

doc->Save(get_ArtifactsDir() + u"Charts.ResetDataPointFill.docx");
```

## Siehe auch

* Class [ChartFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
