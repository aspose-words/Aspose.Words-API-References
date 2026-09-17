---
title: "Aspose::Words::TableStyle::get_ColumnStripe méthode"
linktitle: "get_ColumnStripe"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TableStyle::get_ColumnStripe méthode. Obtient ou définit le nombre de colonnes à inclure dans la bande lorsque le style spécifie une bande de colonnes impaires/paires en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/tablestyle/get_columnstripe/
---
## TableStyle::get_ColumnStripe method


Obtient ou définit le nombre de colonnes à inclure dans le banding lorsque le style spécifie le banding des colonnes impaires/paires.

```cpp
int32_t Aspose::Words::TableStyle::get_ColumnStripe()
```


## Exemples



Montre comment créer des styles de tableau conditionnels qui alternent entre les lignes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nous pouvons configurer un style conditionnel d'un tableau pour appliquer une couleur différente à la ligne/colonne,
// en fonction de si la ligne/colonne est paire ou impaire, créant un motif de couleur alterné.
// Nous pouvons également appliquer un nombre n à la bande de lignes/colonnes,
// signifiant que la couleur alterne après chaque n lignes/colonnes au lieu d'une seule.
// Créez un tableau où les colonnes et les lignes uniques seront regroupées par bandes de trois.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
for (int32_t i = 0; i < 15; i++)
{
    for (int32_t j = 0; j < 4; j++)
    {
        builder->InsertCell();
        builder->Writeln(System::String::Format(u"{0} column.", (j % 2 == 0 ? System::String(u"Even") : System::String(u"Odd"))));
        builder->Write(System::String::Format(u"Row banding {0}.", (i % 3 == 0 ? System::String(u"start") : System::String(u"continuation"))));
    }
    builder->EndRow();
}
builder->EndTable();

// Appliquez un style de ligne à toutes les bordures du tableau.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);

// Définissez les deux couleurs, qui alterneront toutes les 3 lignes.
tableStyle->set_RowStripe(3);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::OddRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightCyan());

// Définissez une couleur à appliquer à chaque colonne paire, qui remplacera toute coloration personnalisée des lignes.
tableStyle->set_ColumnStripe(1);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenColumnBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSalmon());

table->set_Style(tableStyle);

// La propriété "StyleOptions" active la bande de lignes par défaut.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Utilisez également la propriété "StyleOptions" pour activer la bande de colonnes.
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::ColumnBands);

doc->Save(get_ArtifactsDir() + u"Table.AlternatingRowStyles.docx");
```

## Voir aussi

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
