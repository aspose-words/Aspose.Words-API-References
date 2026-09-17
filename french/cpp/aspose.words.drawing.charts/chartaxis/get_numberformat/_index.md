---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat méthode"
linktitle: "get_NumberFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat méthode. Retourne un objet ChartNumberFormat qui permet de définir les formats numériques pour l'axe en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words.drawing.charts/chartaxis/get_numberformat/
---
## ChartAxis::get_NumberFormat method


Retourne un objet [ChartNumberFormat](../../chartnumberformat/) qui permet de définir les formats numériques pour l'axe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartNumberFormat> Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat()
```


## Exemples



Montre comment définir le formatage des valeurs du graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique vierge.
chart->get_Series()->Clear();

// Ajouter une série personnalisée au graphique avec des catégories pour l'axe X,
// et de grandes valeurs numériques respectives pour l'axe Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// Définir le format numérique des libellés des graduations de l'axe Y pour ne pas regrouper les chiffres avec des virgules.
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// Ce drapeau peut remplacer la valeur ci‑dessus et extraire le format numérique de la cellule source.
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(get_ArtifactsDir() + u"Charts.SetNumberFormatToChartAxis.docx");
```

## Voir aussi

* Class [ChartNumberFormat](../../chartnumberformat/)
* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
