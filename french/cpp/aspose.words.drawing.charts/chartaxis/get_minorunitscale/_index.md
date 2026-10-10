---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale méthode"
linktitle: "get_MinorUnitScale"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale méthode. Retourne ou définit la valeur d'échelle pour les petites marques de graduation sur l'axe de catégorie temporelle en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.drawing.charts/chartaxis/get_minorunitscale/
---
## ChartAxis::get_MinorUnitScale method


Obtient ou définit la valeur d'échelle pour les marques de graduation mineures sur l'axe des catégories temporelles.

```cpp
Aspose::Words::Drawing::Charts::AxisTimeUnit Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale()
```


## Exemples



Montre comment manipuler les marques de graduation et les valeurs affichées d'un axe de graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());

// Définissez les petites marques de graduation de l'axe Y pour qu'elles pointent à l'extérieur de la zone du tracé,
// et les grandes marques de graduation pour qu'elles traversent l'axe.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisY();
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);

// Définissez l'axe Y pour afficher une grande marque toutes les 10 unités, et une petite marque toutes les 1 unité.
axis->set_MajorUnit(10);
axis->set_MinorUnit(1);

// Définissez les limites de l'axe Y à -10 et 20.
// Cet axe Y affichera maintenant 4 grandes marques de graduation et 27 petites marques de graduation.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(20.0));

// Pour l'axe X, définissez les grandes marques de graduation toutes les 10 unités,
// et chaque petite marque de graduation toutes les 2,5 unités.
axis = chart->get_AxisX();
axis->set_MajorUnit(10);
axis->set_MinorUnit(2.5);

// Configurez les deux types de marques de graduation pour qu'elles apparaissent à l'intérieur de la zone du tracé du graphique.
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);

// Définissez les limites de l'axe X afin que celui-ci couvre 5 grandes marques de graduation et 12 petites marques de graduation.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(30.0));
axis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

ASSERT_EQ(1, axis->get_TickLabels()->get_Spacing());
ASPOSE_ASSERT_EQ(doc, axis->get_DisplayUnit()->get_Document());

// Définissez les étiquettes de graduation pour afficher leur valeur en millions.
axis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Millions);

// Nous pouvons définir une valeur plus précise selon laquelle les étiquettes de graduation afficheront leurs valeurs.
// Cette instruction est équivalente à celle ci‑dessus.
axis->get_DisplayUnit()->set_CustomUnit(1000000);

doc->Save(get_ArtifactsDir() + u"Charts.AxisDisplayUnit.docx");
```

## Voir aussi

* Enum [AxisTimeUnit](../../axistimeunit/)
* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
