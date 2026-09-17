---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt méthode"
linktitle: "get_CrossesAt"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt method. Spécifie où sur l'axe perpendiculaire l'axe croise en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.drawing.charts/chartaxis/get_crossesat/
---
## ChartAxis::get_CrossesAt method


Spécifie où sur l'axe perpendiculaire l'axe croise.

```cpp
double Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt()
```

## Remarques


La propriété n'a d'effet que si [Crosses](../get_crosses/) est défini sur [Custom](../../axiscrosses/). Elle n'est pas prise en charge par les nouveaux graphiques de MS Office 2016.

Les unités sont déterminées par le type d'axe. Lorsque l'axe est un axe de valeurs, la valeur de la propriété est un nombre décimal sur l'axe de valeurs. Lorsque l'axe est un axe de catégorie temporelle, la valeur est définie comme un nombre entier de jours relatif à la date de base (30/12/1899). Pour un axe de catégorie texte, la valeur est un numéro de catégorie entier, commençant à 1 pour la première catégorie.

## Exemples



Montre comment faire croiser un axe de graphique à un emplacement personnalisé.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Pour les graphiques à colonnes, l'axe Y croise zéro par défaut,
// ce qui signifie que les colonnes pour toutes les valeurs inférieures à zéro pointent vers le bas pour représenter les valeurs négatives.
// Nous pouvons définir une valeur différente pour le croisement de l'axe Y. Dans ce cas, nous le définirons à 3.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisX();
axis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Custom);
axis->set_CrossesAt(3);
axis->set_AxisBetweenCategories(true);

doc->Save(get_ArtifactsDir() + u"Charts.AxisCross.docx");
```

## Voir aussi

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
