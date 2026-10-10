---
title: "Méthode Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined"
linktitle: "get_IsDefined"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined. Obtient un indicateur indiquant si un format est défini en C++."
type: docs
weight: 2250
url: /fr/cpp/aspose.words.drawing.charts/chartformat/get_isdefined/
---
## ChartFormat::get_IsDefined method


Obtient un indicateur indiquant si un format est défini.

```cpp
bool Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined()
```


## Exemples



Montre comment réinitialiser le remplissage à la valeur par défaut définie dans la série.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = series->get_DataPoints()->idx_get(1);

ASSERT_TRUE(dataPoint->get_Format()->get_IsDefined());

dataPoint->get_Format()->SetDefaultFill();

doc->Save(get_ArtifactsDir() + u"Charts.ResetDataPointFill.docx");
```

## Voir aussi

* Class [ChartFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
