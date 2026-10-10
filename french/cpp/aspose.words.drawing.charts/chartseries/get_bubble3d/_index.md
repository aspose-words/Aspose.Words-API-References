---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D méthode"
linktitle: "get_Bubble3D"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D méthode. Spécifie si les bulles dans le graphique à bulles doivent avoir un effet 3-D appliqué en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing.charts/chartseries/get_bubble3d/
---
## ChartSeries::get_Bubble3D method


Spécifie si les bulles dans le graphique à bulles doivent avoir un effet 3D appliqué.

```cpp
bool Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D() override
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

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
