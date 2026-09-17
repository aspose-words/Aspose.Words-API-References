---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion méthode"
linktitle: "get_Bubble3D"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion méthode. Spécifie la distance à laquelle le point de données doit être déplacé depuis le centre du secteur. Peut être négatif, un négatif signifie que la propriété n'est pas définie et qu'aucune explosion ne doit être appliquée. S'applique uniquement aux graphiques circulaires en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing.charts/ichartdatapoint/get_bubble3d/
---
## IChartDataPoint::get_Bubble3D method


Spécifie si les bulles dans le graphique à bulles doivent avoir un effet 3D appliqué.

```cpp
virtual bool Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D()=0
```


## Exemples



Montre comment utiliser les effets 3D avec les graphiques à bulles.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_TRUE(chart->get_Series()->idx_get(0)->get_Bubble3D());

// Appliquez une étiquette de données à chaque bulle affichant son diamètre.
for (int32_t i = 0; i < 3; i++)
{
    chart->get_Series()->idx_get(0)->set_HasDataLabels(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->set_ShowBubbleSize(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->get_Font()->set_Size(12);
}

doc->Save(get_ArtifactsDir() + u"Charts.Bubble3D.docx");
```

## Voir aussi

* Interface [IChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
