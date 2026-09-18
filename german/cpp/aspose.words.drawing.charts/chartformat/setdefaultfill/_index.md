---
title: "Aspose::Words::Drawing::Charts::ChartFormat::SetDefaultFill Methode"
linktitle: "SetDefaultFill"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartFormat::SetDefaultFill Methode. Setzt die Füllung des Diagrammelements auf den Standardwert in C++ zurück."
type: docs
weight: 7000
url: /de/cpp/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat::SetDefaultFill method


Setzt die Füllung des Diagrammelements auf den Standardwert zurück.

```cpp
void Aspose::Words::Drawing::Charts::ChartFormat::SetDefaultFill()
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
