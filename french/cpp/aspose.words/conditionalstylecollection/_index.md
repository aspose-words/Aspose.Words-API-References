---
title: "Classe Aspose::Words::ConditionalStyleCollection"
linktitle: "ConditionalStyleCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::ConditionalStyleCollection. Représente une collection d'objets ConditionalStyle. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class


Représente une collection d'objets [ConditionalStyle](../conditionalstyle/). Pour en savoir plus, consultez l'article de documentation [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::ConditionalStyle>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Efface tous les styles conditionnels du style de tableau. |
| [get_BottomLeftCell](./get_bottomleftcell/)() | Obtient le style de la cellule en bas à gauche. |
| [get_BottomRightCell](./get_bottomrightcell/)() | Obtient le style de la cellule en bas à droite. |
| [get_Count](./get_count/)() const | Obtient le nombre de styles conditionnels dans la collection. |
| [get_EvenColumnBanding](./get_evencolumnbanding/)() | Obtient le style de bande de colonne paire. |
| [get_EvenRowBanding](./get_evenrowbanding/)() | Obtient le style de bande des lignes paires. |
| [get_FirstColumn](./get_firstcolumn/)() | Obtient le style de la première colonne. |
| [get_FirstRow](./get_firstrow/)() | Obtient le style de la première ligne. |
| [get_LastColumn](./get_lastcolumn/)() | Obtient le style de la dernière colonne. |
| [get_LastRow](./get_lastrow/)() | Obtient le style de la dernière ligne. |
| [get_OddColumnBanding](./get_oddcolumnbanding/)() | Obtient le style de bande des colonnes impaires. |
| [get_OddRowBanding](./get_oddrowbanding/)() | Obtient le style de bande des lignes impaires. |
| [get_TopLeftCell](./get_topleftcell/)() | Obtient le style de la cellule en haut à gauche. |
| [get_TopRightCell](./get_toprightcell/)() | Obtient le style de la cellule en haut à droite. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les styles conditionnels de la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::ConditionalStyleType) | Récupère un objet [ConditionalStyle](../conditionalstyle/) par type de style conditionnel. |
| [idx_get](./idx_get/)(int32_t) | Récupère un objet [ConditionalStyle](../conditionalstyle/) par indice. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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
