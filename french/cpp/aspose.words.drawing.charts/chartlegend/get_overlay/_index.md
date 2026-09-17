---
title: "Méthode Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay"
linktitle: "get_Overlay"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay. Détermine si d'autres éléments du graphique sont autorisés à chevaucher la légende. La valeur par défaut est false en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.drawing.charts/chartlegend/get_overlay/
---
## ChartLegend::get_Overlay method


Détermine si d'autres éléments du graphique doivent être autorisés à chevaucher la légende. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay() const
```


## Exemples



Montre comment modifier l'apparence de la légende d'un graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Déplacez la légende du graphique vers le coin supérieur droit.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Donnez plus d'espace aux autres éléments du graphique, comme le tracé, en leur permettant de chevaucher la légende.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## Voir aussi

* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
