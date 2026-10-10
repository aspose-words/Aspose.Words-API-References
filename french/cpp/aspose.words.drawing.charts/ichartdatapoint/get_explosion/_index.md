---
title: "Montre comment déplacer les tranches d'un graphique circulaire depuis le centre."
linktitle: "get_Explosion"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "\"Slices\" d'un graphique circulaire peuvent être déplacées du centre d'une distance via l'attribut Explosion du point de données correspondant."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.drawing.charts/ichartdatapoint/get_explosion/
---
## IChartDataPoint::get_Explosion method


Spécifie la distance à laquelle le point de données doit être déplacé depuis le centre du secteur. Peut être négatif, un négatif signifie que la propriété n'est pas définie et qu'aucune explosion ne doit être appliquée. S'applique uniquement aux graphiques en secteurs.

```cpp
virtual int32_t Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion()=0
```


## Exemples



Ajoutez un point de données à la première portion du graphique circulaire et déplacez-le du centre de 10 points.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Sales", chart->get_Series()->idx_get(0)->get_Name());

// "Slices" d'un diagramme circulaire peuvent être déplacées du centre d'une distance via l'attribut Explosion du point de données correspondant.
// Ajoutez un point de données à la première portion du diagramme circulaire et déplacez‑le du centre de 10 points.
// Aspose.Words crée automatiquement des points de données s'ils n'existent pas.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(0);
dataPoint->set_Explosion(10);

// Déplacez la deuxième portion d'une plus grande distance.
dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(1);
dataPoint->set_Explosion(40);

doc->Save(get_ArtifactsDir() + u"Charts.PieChartExplosion.docx");
```

## Voir aussi

* Interface [IChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
