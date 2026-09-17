---
title: "classe Aspose::Words::TableStyle"
linktitle: "TableStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::TableStyle. Représente un style de tableau. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 67000
url: /fr/cpp/aspose.words/tablestyle/
---
## TableStyle class


Représente un style de tableau. Pour en savoir plus, consultez l'article de documentation [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class TableStyle : public Aspose::Words::Style,
                   public Aspose::Words::ICellAttrSource,
                   public Aspose::Words::IRowAttrSource,
                   public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Equals](../style/equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Compare avec le style spécifié. Les Istds de styles sont comparés uniquement pour les styles intégrés. Les valeurs par défaut des styles ne sont pas incluses dans la comparaison. Le style de base, le style lié et le style du paragraphe suivant sont comparés de manière récursive. |
| [get_Aliases](../style/get_aliases/)() | Obtient tous les alias de ce style. Si le style n’a aucun alias, un tableau vide de chaînes est retourné. |
| [get_Alignment](./get_alignment/)() | Spécifie l'alignement du style de tableau. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Obtient ou définit un indicateur indiquant si le texte d'une ligne de tableau peut se diviser à travers un saut de page. |
| [get_AutomaticallyUpdate](../style/get_automaticallyupdate/)() const | Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée. |
| [get_BaseStyleName](../style/get_basestylename/)() | Obtient/definit le nom du style sur lequel ce style est basé. |
| [get_Borders](./get_borders/)() | Obtient la collection des bordures de cellules par défaut pour le style. |
| [get_BottomPadding](./get_bottompadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter sous le contenu des cellules du tableau. |
| [get_BuiltIn](../style/get_builtin/)() | Vrai si ce style fait partie des styles intégrés dans MS Word. |
| [get_CellSpacing](./get_cellspacing/)() | Obtient ou définit la quantité d'espace (en points) entre les cellules. |
| [get_ColumnStripe](./get_columnstripe/)() | Obtient ou définit le nombre de colonnes à inclure dans le banding lorsque le style spécifie le banding des colonnes impaires/paires. |
| [get_ConditionalStyles](./get_conditionalstyles/)() | Collection de styles conditionnels qui peuvent être définis pour ce style de tableau. |
| [get_Document](../style/get_document/)() | Obtient le document propriétaire. |
| [get_Font](../style/get_font/)() | Obtient le formatage de caractères du style. |
| [get_IsHeading](../style/get_isheading/)() | Vrai lorsque le style fait partie des styles de titre intégrés. |
| [get_IsQuickStyle](../style/get_isquickstyle/)() const | Spécifie si ce style est affiché dans la galerie Rapide [Style](../style/) de l'interface MS Word. |
| [get_LeftIndent](./get_leftindent/)() | Obtient ou définit la valeur qui représente le retrait gauche d'un tableau. |
| [get_LeftPadding](./get_leftpadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter à gauche du contenu des cellules du tableau. |
| [get_LinkedStyleName](../style/get_linkedstylename/)() | Obtient/définit le nom du [Style](../style/) lié à celui-ci. Retourne une chaîne vide si aucun style n'est lié. |
| [get_List](../style/get_list/)() | Obtient la liste qui définit le formatage de ce style de liste. |
| [get_ListFormat](../style/get_listformat/)() | Fournit l’accès aux propriétés de formatage de liste d’un style de paragraphe. |
| [get_Locked](../style/get_locked/)() const | Spécifie si ce style est verrouillé. |
| [get_Name](../style/get_name/)() const | Obtient ou définit le nom du style. |
| [get_NextParagraphStyleName](../style/get_nextparagraphstylename/)() | Obtient/definit le nom du style à appliquer automatiquement à un nouveau paragraphe inséré après un paragraphe formaté avec le style spécifié. |
| [get_ParagraphFormat](../style/get_paragraphformat/)() | Obtient le formatage du paragraphe du style. |
| [get_Priority](../style/get_priority/)() const | Obtient/definit la valeur entière qui représente la priorité de tri des styles dans le volet des tâches Styles. |
| [get_RightPadding](./get_rightpadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter à droite du contenu des cellules du tableau. |
| [get_RowStripe](./get_rowstripe/)() | Obtient ou définit le nombre de lignes à inclure dans le banding lorsque le style spécifie le banding des lignes impaires/paires. |
| [get_SemiHidden](../style/get_semihidden/)() const | Obtient/definit si le style est masqué dans la galerie des Styles et dans le volet des Styles. |
| [get_Shading](./get_shading/)() | Obtient un objet [Shading](../shading/) qui fait référence au format de remplissage des cellules de tableau. |
| [get_StyleIdentifier](../style/get_styleidentifier/)() const | Obtient l'identifiant de style indépendant de la locale pour un style intégré. |
| [get_Styles](../style/get_styles/)() const | Obtient la collection de styles à laquelle ce style appartient. |
| [get_TopPadding](./get_toppadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules du tableau. |
| [get_Type](../style/get_type/)() const | Obtient le type de style (paragraphe ou caractère). |
| [get_UnhideWhenUsed](../style/get_unhidewhenused/)() const | Obtient/definit si le style utilisé dans le document actuel se dévoile dans la galerie des Styles et dans le volet des Styles. Vrai lorsque le style utilisé doit être affiché dans la galerie des Styles. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Spécifie l'alignement vertical des cellules. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../style/remove/)() | Supprime le style spécifié du document. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | Mutateur pour [Aspose::Words::TableStyle::get_Alignment](./get_alignment/). |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Mutateur pour [Aspose::Words::TableStyle::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_AutomaticallyUpdate](../style/set_automaticallyupdate/)(bool) | Mutateur pour [Aspose::Words::Style::get_AutomaticallyUpdate](../style/get_automaticallyupdate/). |
| [set_BaseStyleName](../style/set_basestylename/)(const System::String\&) | Mutateur pour [Aspose::Words::Style::get_BaseStyleName](../style/get_basestylename/). |
| [set_BottomPadding](./set_bottompadding/)(double) | Mutateur pour [Aspose::Words::TableStyle::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | Mutateur pour [Aspose::Words::TableStyle::get_CellSpacing](./get_cellspacing/). |
| [set_ColumnStripe](./set_columnstripe/)(int32_t) | Mutateur pour [Aspose::Words::TableStyle::get_ColumnStripe](./get_columnstripe/). |
| [set_IsQuickStyle](../style/set_isquickstyle/)(bool) | Mutateur pour [Aspose::Words::Style::get_IsQuickStyle](../style/get_isquickstyle/). |
| [set_LeftIndent](./set_leftindent/)(double) | Mutateur pour [Aspose::Words::TableStyle::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Mutateur pour [Aspose::Words::TableStyle::get_LeftPadding](./get_leftpadding/). |
| [set_LinkedStyleName](../style/set_linkedstylename/)(const System::String\&) | Mutateur pour [Aspose::Words::Style::get_LinkedStyleName](../style/get_linkedstylename/). |
| [set_Locked](../style/set_locked/)(bool) | Mutateur pour [Aspose::Words::Style::get_Locked](../style/get_locked/). |
| [set_Name](../style/set_name/)(const System::String\&) | Mutateur pour [Aspose::Words::Style::get_Name](../style/get_name/). |
| [set_NextParagraphStyleName](../style/set_nextparagraphstylename/)(const System::String\&) | Mutateur pour [Aspose::Words::Style::get_NextParagraphStyleName](../style/get_nextparagraphstylename/). |
| [set_Priority](../style/set_priority/)(int32_t) | Mutateur pour [Aspose::Words::Style::get_Priority](../style/get_priority/). |
| [set_RightPadding](./set_rightpadding/)(double) | Mutateur pour [Aspose::Words::TableStyle::get_RightPadding](./get_rightpadding/). |
| [set_RowStripe](./set_rowstripe/)(int32_t) | Mutateur pour [Aspose::Words::TableStyle::get_RowStripe](./get_rowstripe/). |
| [set_SemiHidden](../style/set_semihidden/)(bool) | Mutateur pour [Aspose::Words::Style::get_SemiHidden](../style/get_semihidden/). |
| [set_TopPadding](./set_toppadding/)(double) | Mutateur pour [Aspose::Words::TableStyle::get_TopPadding](./get_toppadding/). |
| [set_UnhideWhenUsed](../style/set_unhidewhenused/)(bool) | Mutateur pour [Aspose::Words::Style::get_UnhideWhenUsed](../style/get_unhidewhenused/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Mutateur pour [Aspose::Words::TableStyle::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment créer des paramètres de style personnalisés pour le tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// La définition des propriétés de style d'un tableau peut affecter les propriétés du tableau lui‑même.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Voir aussi

* Class [Style](../style/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
