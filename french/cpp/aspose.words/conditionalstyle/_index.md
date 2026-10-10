---
title: "Aspose::Words::ConditionalStyle class"
linktitle: "ConditionalStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::ConditionalStyle. Représente un formatage spécial appliqué à une zone d'un tableau avec le style de tableau assigné. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words/conditionalstyle/
---
## ConditionalStyle class


Représente un formatage spécial appliqué à une zone d'un tableau avec un style de tableau attribué. Pour en savoir plus, consultez l'article de documentation [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyle : public Aspose::Words::IBorderAttrSource,
                         public Aspose::Words::IShadingAttrSource,
                         public Aspose::Words::IParaAttrSource,
                         public Aspose::Words::IRunAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Efface le formatage de ce style conditionnel. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Compare ce style conditionnel avec l'objet spécifié. |
| [get_Borders](./get_borders/)() | Obtient la collection des bordures de cellule par défaut pour le style conditionnel. |
| [get_BottomPadding](./get_bottompadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter sous le contenu des cellules du tableau. |
| [get_Font](./get_font/)() | Obtient le formatage des caractères du style conditionnel. |
| [get_LeftPadding](./get_leftpadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter à gauche du contenu des cellules du tableau. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Obtient le formatage du paragraphe du style conditionnel. |
| [get_RightPadding](./get_rightpadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter à droite du contenu des cellules du tableau. |
| [get_Shading](./get_shading/)() | Obtient un objet [Shading](../shading/) qui fait référence au formatage d'ombrage pour ce style conditionnel. |
| [get_TopPadding](./get_toppadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules du tableau. |
| [get_Type](./get_type/)() | Obtient la zone du tableau à laquelle ce style conditionnel se rapporte. |
| [GetHashCode](./gethashcode/)() const override | Calcule le code de hachage pour cet objet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Définisseur pour [Aspose::Words::ConditionalStyle::get_BottomPadding](./get_bottompadding/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Définisseur pour [Aspose::Words::ConditionalStyle::get_LeftPadding](./get_leftpadding/). |
| [set_RightPadding](./set_rightpadding/)(double) | Définisseur pour [Aspose::Words::ConditionalStyle::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Définisseur pour [Aspose::Words::ConditionalStyle::get_TopPadding](./get_toppadding/). |
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
