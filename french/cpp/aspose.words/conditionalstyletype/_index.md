---
title: "Aspose::Words::ConditionalStyleType enum"
linktitle: "ConditionalStyleType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ConditionalStyleType enum. Représente les zones de tableau possibles auxquelles un formatage conditionnel peut être défini dans un style de tableau en C++."
type: docs
weight: 85000
url: /fr/cpp/aspose.words/conditionalstyletype/
---
## ConditionalStyleType enum


Représente les zones de tableau possibles auxquelles une mise en forme conditionnelle peut être définie dans un style de tableau.

```cpp
enum class ConditionalStyleType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| FirstRow | 0 | Spécifie le format de la première ligne d'un tableau. |
| FirstColumn | 1 | Spécifie le format de la première colonne d'un tableau. |
| LastRow | 2 | Spécifie le format de la dernière ligne d'un tableau. |
| LastColumn | 3 | Spécifie le format de la dernière colonne d'un tableau. |
| OddRowBanding | 4 | Spécifie le format de la bande de lignes impaires. |
| OddColumnBanding | 5 | Spécifie le format de la bande de colonnes impaires. |
| EvenRowBanding | 6 | Spécifie le format de la bande de lignes paires. |
| EvenColumnBanding | 7 | Spécifie le formatage de la bande de colonne paire. |
| TopLeftCell | 8 | Spécifie le formatage de la cellule supérieure gauche d'un tableau. |
| TopRightCell | 9 | Spécifie le formatage de la cellule supérieure droite d'un tableau. |
| BottomLeftCell | 10 | Spécifie le formatage de la cellule inférieure gauche d'un tableau. |
| BottomRightCell | 11 | Spécifie le formatage de la cellule inférieure droite d'un tableau. |


## Exemples



Montre comment travailler avec certains styles de zone d'un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Cell 3");
builder->InsertCell();
builder->Write(u"Cell 4");
builder->EndTable();

// Créez un style de tableau personnalisé.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));

// Les styles conditionnels sont des changements de formatage qui n'affectent que certaines cellules du tableau.
// basés sur un prédicat, comme le fait que les cellules soient dans la dernière ligne.
// Voici trois façons d'accéder aux styles conditionnels d'un style de tableau depuis la collection "ConditionalStyles".
// 1 -  Par type de style :
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::FirstRow)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AliceBlue());

// 2 -  Par indice :
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
ASSERT_EQ(Aspose::Words::ConditionalStyleType::FirstRow, tableStyle->get_ConditionalStyles()->idx_get(0)->get_Type());

// 3 -  En tant que propriété :
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// Appliquez le remplissage et le formatage du texte aux styles conditionnels.
tableStyle->get_ConditionalStyles()->get_LastRow()->set_BottomPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_LeftPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_RightPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_TopPadding(10);
tableStyle->get_ConditionalStyles()->get_LastColumn()->get_Font()->set_Bold(true);

// Listez toutes les conditions de style possibles.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::ConditionalStyle>>> enumerator = tableStyle->get_ConditionalStyles()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::ConditionalStyle> currentStyle = enumerator->get_Current();
        if (currentStyle != nullptr)
        {
            std::cout << System::EnumGetName(currentStyle->get_Type()) << std::endl;
        }
    }
}

// Appliquez le style personnalisé, qui contient tous les styles conditionnels, au tableau.
table->set_Style(tableStyle);

// Notre style applique certains styles conditionnels par défaut.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Nous devrons activer tous les autres styles nous-mêmes via la propriété "StyleOptions".
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::LastRow | Aspose::Words::Tables::TableStyleOptions::LastColumn);

doc->Save(get_ArtifactsDir() + u"Table.ConditionalStyles.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
