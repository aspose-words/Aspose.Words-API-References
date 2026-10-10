---
title: "Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined yöntemi"
linktitle: "get_IsDefined"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined yöntemi. C++'ta herhangi bir formatın tanımlı olup olmadığını gösteren bir bayrak alır."
type: docs
weight: 2250
url: /tr/cpp/aspose.words.drawing.charts/chartformat/get_isdefined/
---
## ChartFormat::get_IsDefined method


Herhangi bir biçimin tanımlanıp tanımlanmadığını gösteren bir bayrak alır.

```cpp
bool Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined()
```


## Örnekler



Seride tanımlanan varsayılan değere dolgu sıfırlamayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = series->get_DataPoints()->idx_get(1);

ASSERT_TRUE(dataPoint->get_Format()->get_IsDefined());

dataPoint->get_Format()->SetDefaultFill();

doc->Save(get_ArtifactsDir() + u"Charts.ResetDataPointFill.docx");
```

## Ayrıca Bakınız

* Class [ChartFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
