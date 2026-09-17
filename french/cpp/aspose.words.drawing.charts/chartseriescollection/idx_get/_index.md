---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::idx_get method"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::idx_get method. Renvoie un ChartSeries à l'index spécifié en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.drawing.charts/chartseriescollection/idx_get/
---
## ChartSeriesCollection::idx_get method


Renvoie un [ChartSeries](../../chartseries/) à l'index spécifié.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::idx_get(int32_t index)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | Un index dans la collection. |
## Remarques


L'index commence à zéro.

Les index négatifs sont autorisés et indiquent un accès depuis la fin de la collection. Par exemple, -1 signifie le dernier élément, -2 le deuxième avant le dernier, etc.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

## Exemples



Montre comment ajouter et supprimer des données de séries dans un graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un graphique à colonnes qui contiendra trois séries de données de démonstration par défaut.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Chaque série possède quatre valeurs décimales : une pour chacune des quatre catégories.
// Quatre groupes de trois colonnes représenteront ces données.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> chartData = chart->get_Series();

ASSERT_EQ(3, chartData->get_Count());

// Imprimez le nom de chaque série du graphique.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>> enumerator = chart->get_Series()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current()->get_Name() << std::endl;
    }
}

// Voici les noms des catégories du graphique.
System::ArrayPtr<System::String> categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});

// Nous pouvons ajouter une série avec de nouvelles valeurs pour les catégories existantes.
// Ce graphique contiendra maintenant quatre groupes de quatre colonnes.
chart->get_Series()->Add(u"Series 4", categories, System::MakeArray<double>({4.4, 7.0, 3.5, 2.1}));

// Une série de graphique peut également être supprimée par indice, comme ceci.
// Cela supprimera l'une des trois séries de démonstration qui accompagnent le graphique.
chartData->RemoveAt(2);

ASSERT_FALSE(chartData->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s) -> bool
{
    return s->get_Name() == u"Series 3";
}))));

// Nous pouvons également effacer toutes les données du graphique d'un coup avec cette méthode.
// Lors de la création d'un nouveau graphique, voici comment effacer toutes les données de démonstration
// avant de pouvoir commencer à travailler sur un graphique vierge.
chartData->Clear();
```

## Voir aussi

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
