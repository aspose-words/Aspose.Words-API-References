---
title: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class"
linktitle: "BubbleSizeCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class. Représente une collection de tailles de bulles pour une série de graphique en C++."
type: docs
weight: 3500
url: /fr/cpp/aspose.words.drawing.charts/bubblesizecollection/
---
## BubbleSizeCollection class


Représente une collection de tailles de bulles pour une série de graphique.

```cpp
class BubbleSizeCollection : public System::Collections::Generic::IEnumerable<double>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Count](./get_count/)() | Obtient le nombre d'éléments dans cette collection. |
| [get_FormatCode](./get_formatcode/)() | Obtient ou définit le code de format appliqué aux tailles de bulles. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtient ou définit la valeur de la taille de bulle à l'index spécifié. |
| [idx_set](./idx_set/)(int32_t, double) | Obtient ou définit la valeur de la taille de bulle à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Mutateur pour [Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Remarques


La collection ne permet que de modifier les tailles des bulles. Pour ajouter ou insérer de nouvelles valeurs à une série de graphique, ou supprimer des valeurs, les méthodes appropriées de la classe [ChartSeries](../chartseries/) peuvent être utilisées.

Les valeurs de taille de bulle vides sont représentées par **NaN**.

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
