---
title: "Aspose::Words::Drawing::Charts::AxisBuiltInUnit enum"
linktitle: "AxisBuiltInUnit"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::AxisBuiltInUnit enum. Spécifie les unités d'affichage pour un axe en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enum


Spécifie les unités d'affichage pour un axe.

```cpp
enum class AxisBuiltInUnit
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Spécifie que les valeurs du graphique doivent être affichées telles quelles. |
| Personnalisé | 1 | Spécifie que les valeurs du graphique doivent être divisées par un diviseur défini par l'utilisateur. Cette valeur n'est pas prise en charge par les nouveaux types de graphiques de MS Office 2016. |
| Billions | 2 | Spécifie que les valeurs du graphique doivent être divisées par 1 000 000 000. |
| HundredMillions | 3 | Spécifie que les valeurs du graphique doivent être divisées par 100 000 000. |
| Hundreds | 4 | Spécifie que les valeurs du graphique doivent être divisées par 100. |
| HundredThousands | 5 | Spécifie que les valeurs du graphique doivent être divisées par 100 000. |
| Millions | 6 | Spécifie que les valeurs du graphique doivent être divisées par 1 000 000. |
| TenMillions | 7 | Spécifie que les valeurs du graphique doivent être divisées par 10 000 000. |
| TenThousands | 8 | Spécifie que les valeurs du graphique doivent être divisées par 10 000. |
| Thousands | 9 | Spécifie que les valeurs du graphique doivent être divisées par 1 000. |
| Trillions | 10 | Spécifie que les valeurs du graphique doivent être divisées par 1 000 000 000 0000. |
| Percentage | 11 | Spécifie que les valeurs du graphique doivent être divisées par 0,01. Cette valeur n’est prise en charge que par les nouveaux types de graphiques de MS Office 2016. |


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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
