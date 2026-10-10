---
title: "Aspose::Words::Drawing::Charts::ChartMultilevelValue class"
linktitle: "ChartMultilevelValue"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartMultilevelValue class. Représente une valeur pour les graphiques affichant des données à plusieurs niveaux en C++."
type: docs
weight: 14500
url: /fr/cpp/aspose.words.drawing.charts/chartmultilevelvalue/
---
## ChartMultilevelValue class


Représente une valeur pour les graphiques affichant des données à plusieurs niveaux.

```cpp
class ChartMultilevelValue : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&, const System::String\&, const System::String\&) | Initialise une nouvelle instance de cette classe qui représente une valeur à trois niveaux. |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&, const System::String\&) | Initialise une nouvelle instance de cette classe qui représente une valeur à deux niveaux. |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&) | Initialise une nouvelle instance de cette classe qui représente une valeur à un seul niveau. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Obtient un indicateur indiquant si l'objet spécifié est égal à l'objet de données multiniveau actuel. |
| [get_Level1](./get_level1/)() const | Obtient le nom du niveau supérieur du graphique auquel cette valeur se réfère. |
| [get_Level2](./get_level2/)() const | Obtient le nom du niveau intermédiaire du graphique auquel cette valeur se réfère. |
| [get_Level3](./get_level3/)() const | Obtient le nom du niveau inférieur du graphique auquel cette valeur se réfère. |
| [GetHashCode](./gethashcode/)() const override | Obtient un code de hachage pour l'objet de données multiniveau actuel. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exemples



Montre comment créer un graphique en carte d'arbres.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer un graphique en carte d'arbres.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Treemap, 450, 280);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"World Population");

// Supprimer la série générée par défaut.
chart->get_Series()->Clear();

// Ajouter une série.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Population by Region", System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>>({System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"China"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"India"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Indonesia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Pakistan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Bangladesh"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Japan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Philippines"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Nigeria"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Ethiopia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Egypt"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Russia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Germany"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Brazil"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Mexico"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"United States", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Oceania")}), System::MakeArray<double>({1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000, 223800000, 107334000, 105914499, 903000000, 146150789, 84607016, 516000000, 203080756, 129713690, 310000000, 335893238, 35000000, 42000000}));

// Afficher les étiquettes de données.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowCategoryName(true);
System::String thousandSeparator = System::Globalization::CultureInfo::get_CurrentCulture()->get_NumberFormat()->get_CurrencyGroupSeparator();
series->get_DataLabels()->get_NumberFormat()->set_FormatCode(System::String::Format(u"#{0}0", thousandSeparator));

doc->Save(get_ArtifactsDir() + u"Charts.Treemap.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
