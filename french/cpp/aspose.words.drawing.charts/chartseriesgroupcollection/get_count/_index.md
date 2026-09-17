---
title: "Méthode Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count"
linktitle: "get_Count"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count. Retourne le nombre de groupes de séries dans cette collection en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/get_count/
---
## ChartSeriesGroupCollection::get_Count method


Renvoie le nombre de groupes de séries dans cette collection.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count()
```


## Exemples



Montrez comment supprimer l'axe secondaire.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Combo chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> seriesGroups = chart->get_SeriesGroups();

// Trouvez l'axe secondaire et supprimez-le de la collection.
for (int32_t i = 0; i < seriesGroups->get_Count(); i++)
{
    if (seriesGroups->idx_get(i)->get_AxisGroup() == Aspose::Words::Drawing::Charts::AxisGroup::Secondary)
    {
        seriesGroups->RemoveAt(i);
    }
}
```

## Voir aussi

* Class [ChartSeriesGroupCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
