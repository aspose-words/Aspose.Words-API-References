---
title: "Méthode Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode"
linktitle: "get_FormatCode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode. Obtient ou définit le code de format appliqué à une étiquette de données en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing.charts/chartnumberformat/get_formatcode/
---
## ChartNumberFormat::get_FormatCode method


Obtient ou définit le code de format appliqué à une étiquette de données.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode()
```

## Remarques


Le formatage des nombres est utilisé pour modifier la façon dont une valeur apparaît dans une étiquette de données et peut être utilisé de manières très créatives. Les exemples de formats numériques :

Nombre - "#,##0.00"

Devise - "\"\$\\"#,##0.00"

Heure - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Pourcentage - "0.00%"

Fraction - "# ?/?"

Scientifique - "0.00E+00"

Texte - \"@\"

Comptabilité - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Personnalisé avec couleur - "[Red]-#,##0.0"

## Exemples



Montre comment activer et configurer les étiquettes de données pour une série de graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez un graphique en courbes, puis effacez ses séries de données de démonstration pour commencer avec un graphique vierge,
// et définissez ensuite un titre.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// Insérez une série de graphique personnalisée avec les mois comme catégories pour l'axe X,
// et les montants décimaux correspondants pour l'axe Y.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// Activez les étiquettes de données, puis appliquez un format numérique personnalisé pour les valeurs affichées dans les étiquettes de données.
// Ce format traitera les valeurs décimales affichées comme des millions de dollars américains.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```


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

* Class [ChartNumberFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
