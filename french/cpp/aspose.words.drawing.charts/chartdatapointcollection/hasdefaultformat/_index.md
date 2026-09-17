---
title: "Méthode Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat"
linktitle: "HasDefaultFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat. Obtient un indicateur indiquant si le point de données à l'index spécifié a le format par défaut en C++."
type: docs
weight: 5500
url: /fr/cpp/aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/
---
## ChartDataPointCollection::HasDefaultFormat method


Obtient un indicateur indiquant si le point de données à l'index spécifié possède le format par défaut.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat(int32_t dataPointIndex)
```


## Exemples



Montre comment copier le format du point de données.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

// Obtient le graphique et la série pour mettre à jour le format.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_FALSE(dataPoints->HasDefaultFormat(1));

// Copie le format du point de données avec l'index 1 vers le point de données avec l'index 2
// de sorte que le point de données 2 ressemble au point de données 1.
dataPoints->CopyFormat(0, 1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

// Copiez le format du point de données avec l'index 0 vers les paramètres par défaut de la série afin que tous les points de données
// dans la série, les éléments qui ont le format par défaut ressemblent au point de données 0.
series->CopyFormatFrom(1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

doc->Save(get_ArtifactsDir() + u"Charts.CopyDataPointFormat.docx");
```

## Voir aussi

* Class [ChartDataPointCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
