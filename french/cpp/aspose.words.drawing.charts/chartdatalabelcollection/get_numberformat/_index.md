---
title: "Méthode Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_NumberFormat"
linktitle: "get_NumberFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_NumberFormat. Obtient une instance ChartNumberFormat permettant de définir le format numérique pour les étiquettes de données de toute la série en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_numberformat/
---
## ChartDataLabelCollection::get_NumberFormat method


Obtient une instance [ChartNumberFormat](../../chartnumberformat/) permettant de définir le format numérique pour les étiquettes de données de toute la série.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartNumberFormat> Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_NumberFormat()
```


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

## Voir aussi

* Class [ChartNumberFormat](../../chartnumberformat/)
* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
