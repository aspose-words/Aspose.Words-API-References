---
title: "classe Aspose::Words::Tables::Table"
linktitle: "Table"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Tables::Table. Représente un tableau dans un document Word. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.tables/table/
---
## Table class


Représente un tableau dans un document Word. Pour en savoir plus, consultez l’article de documentation [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class Table : public Aspose::Words::CompositeNode
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter la fin du tableau. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter le début du tableau. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AutoFit](./autofit/)(Aspose::Words::Tables::AutoFitBehavior) | Redimensionne le tableau et les cellules selon le comportement d'ajustement automatique spécifié. |
| [ClearBorders](./clearborders/)() | Supprime toutes les bordures du tableau et des cellules de ce tableau. |
| [ClearShading](./clearshading/)() | Supprime toutes les ombrages du tableau. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [ConvertToHorizontallyMergedCells](./converttohorizontallymergedcells/)() | Convertit les cellules fusionnées horizontalement par largeur en cellules fusionnées par [HorizontalMerge](../cellformat/get_horizontalmerge/). |
| [EnsureMinimum](./ensureminimum/)() | Si le tableau n'a aucune ligne, crée et ajoute une [Row](../row/). |
| [get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/)() | Obtient ou définit la position horizontale absolue du tableau flottant spécifiée par les propriétés du tableau, en points. La valeur par défaut est 0. |
| [get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/)() | Obtient ou définit la position verticale absolue du tableau flottant spécifiée par les propriétés du tableau, en points. La valeur par défaut est 0. |
| [get_Alignment](./get_alignment/)() | Spécifie comment un tableau en ligne est aligné dans le document. |
| [get_AllowAutoFit](./get_allowautofit/)() | Permet à Microsoft Word et à Aspose.Words de redimensionner automatiquement les cellules d'un tableau pour qu'elles s'adaptent à leur contenu. |
| [get_AllowCellSpacing](./get_allowcellspacing/)() | Obtient ou définit l'option "Allow spacing between cells". |
| [get_AllowOverlap](./get_allowoverlap/)() | Obtient si un tableau flottant doit permettre à d'autres objets flottants dans le document de chevaucher ses limites lorsqu'il est affiché. La valeur par défaut est **true**. |
| [get_Bidi](./get_bidi/)() | Obtient ou définit si ce tableau est de droite à gauche. |
| [get_BottomPadding](./get_bottompadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter sous le contenu des cellules. |
| [get_CellSpacing](./get_cellspacing/)() | Obtient ou définit la quantité d'espace (en points) entre les cellules. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Obtient le nombre d'enfants immédiats de ce nœud. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| [get_Description](./get_description/)() | Obtient ou définit la description de ce tableau. Elle fournit une représentation textuelle alternative des informations contenues dans le tableau. |
| [get_DistanceBottom](./get_distancebottom/)() | Obtient ou définit la distance entre le bas du tableau et le texte environnant, en points. |
| [get_DistanceLeft](./get_distanceleft/)() | Obtient ou définit la distance entre le côté gauche du tableau et le texte environnant, en points. |
| [get_DistanceRight](./get_distanceright/)() | Obtient ou définit la distance entre le côté droit du tableau et le texte environnant, en points. |
| [get_DistanceTop](./get_distancetop/)() | Obtient ou définit la distance entre le haut du tableau et le texte environnant, en points. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Obtient le premier enfant du nœud. |
| [get_FirstRow](./get_firstrow/)() | Renvoie le premier nœud [Row](../row/) du tableau. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Renvoie **true** si ce nœud possède des nœuds enfants. |
| [get_HorizontalAnchor](./get_horizontalanchor/)() | Obtient l'objet de base à partir duquel le positionnement horizontal du tableau flottant doit être calculé. La valeur par défaut est [Column](../../aspose.words.drawing/relativehorizontalposition/). |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Renvoie **true** car ce nœud peut avoir des nœuds enfants. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Obtient le dernier enfant du nœud. |
| [get_LastRow](./get_lastrow/)() | Renvoie le dernier nœud [Row](../row/) du tableau. |
| [get_LeftIndent](./get_leftindent/)() | Obtient ou définit la valeur qui représente le retrait gauche du tableau. |
| [get_LeftPadding](./get_leftpadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter à gauche du contenu des cellules. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie [Table](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_PreferredWidth](./get_preferredwidth/)() | Obtient ou définit la largeur préférée du tableau. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Renvoie un objet [Range](../../aspose.words/range/) qui représente la partie d'un document contenue dans ce nœud. |
| [get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/)() | Obtient ou définit l'alignement horizontal relatif du tableau flottant. |
| [get_RelativeVerticalAlignment](./get_relativeverticalalignment/)() | Obtient ou définit l'alignement vertical relatif du tableau flottant. |
| [get_RightPadding](./get_rightpadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter à droite du contenu des cellules. |
| [get_Rows](./get_rows/)() | Fournit un accès typé aux lignes du tableau. |
| [get_Style](./get_style/)() | Obtient ou définit le style de tableau appliqué à ce tableau. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Obtient ou définit l'identifiant de style indépendant de la locale du style de tableau appliqué à ce tableau. |
| [get_StyleName](./get_stylename/)() | Obtient ou définit le nom du style de tableau appliqué à ce tableau. |
| [get_StyleOptions](./get_styleoptions/)() | Obtient ou définit les indicateurs binaires qui spécifient comment un style de tableau est appliqué à ce tableau. |
| [get_TextWrapping](./get_textwrapping/)() | Obtient ou définit [TextWrapping](./get_textwrapping/) pour le tableau. |
| [get_Title](./get_title/)() | Obtient ou définit le titre de ce tableau. Il fournit une représentation textuelle alternative des informations contenues dans le tableau. |
| [get_TopPadding](./get_toppadding/)() | Obtient ou définit la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Obtient l'objet de base à partir duquel le positionnement vertical du tableau flottant doit être calculé. La valeur par défaut est [Margin](../../aspose.words.drawing/relativeverticalposition/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../../aspose.words/nodetype/) spécifié. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Renvoie le nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Fournit une prise en charge de l'itération de type foreach sur les nœuds enfants de ce nœud. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Obtient le texte de ce nœud et de tous ses enfants. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index du nœud enfant spécifié dans le tableau des nœuds enfants. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tous les nœuds descendants [SmartTag](../../aspose.words.markup/smarttag/) du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Sélectionne le premier [Node](../../aspose.words/node/) qui correspond à l'expression XPath. |
| [set_AbsoluteHorizontalDistance](./set_absolutehorizontaldistance/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/). |
| [set_AbsoluteVerticalDistance](./set_absoluteverticaldistance/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | Définisseur pour [Aspose::Words::Tables::Table::get_Alignment](./get_alignment/). |
| [set_AllowAutoFit](./set_allowautofit/)(bool) | Définisseur pour [Aspose::Words::Tables::Table::get_AllowAutoFit](./get_allowautofit/). |
| [set_AllowCellSpacing](./set_allowcellspacing/)(bool) | Définisseur pour [Aspose::Words::Tables::Table::get_AllowCellSpacing](./get_allowcellspacing/). |
| [set_Bidi](./set_bidi/)(bool) | Définisseur pour [Aspose::Words::Tables::Table::get_Bidi](./get_bidi/). |
| [set_BottomPadding](./set_bottompadding/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_CellSpacing](./get_cellspacing/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Mutateur pour [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Description](./set_description/)(const System::String\&) | Définisseur pour [Aspose::Words::Tables::Table::get_Description](./get_description/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_DistanceTop](./get_distancetop/). |
| [set_HorizontalAnchor](./set_horizontalanchor/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Définisseur pour [Aspose::Words::Tables::Table::get_HorizontalAnchor](./get_horizontalanchor/). |
| [set_LeftIndent](./set_leftindent/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_LeftPadding](./get_leftpadding/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Définisseur pour [Aspose::Words::Tables::Table::get_PreferredWidth](./get_preferredwidth/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalAlignment](./set_relativehorizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Définisseur pour [Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/). |
| [set_RelativeVerticalAlignment](./set_relativeverticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Définisseur pour [Aspose::Words::Tables::Table::get_RelativeVerticalAlignment](./get_relativeverticalalignment/). |
| [set_RightPadding](./set_rightpadding/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_RightPadding](./get_rightpadding/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Définisseur pour [Aspose::Words::Tables::Table::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Définisseur pour [Aspose::Words::Tables::Table::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Définisseur pour [Aspose::Words::Tables::Table::get_StyleName](./get_stylename/). |
| [set_StyleOptions](./set_styleoptions/)(Aspose::Words::Tables::TableStyleOptions) | Définisseur pour [Aspose::Words::Tables::Table::get_StyleOptions](./get_styleoptions/). |
| [set_TextWrapping](./set_textwrapping/)(Aspose::Words::Tables::TextWrapping) | Définisseur pour [Aspose::Words::Tables::Table::get_TextWrapping](./get_textwrapping/). |
| [set_Title](./set_title/)(const System::String\&) | Définisseur pour [Aspose::Words::Tables::Table::get_Title](./get_title/). |
| [set_TopPadding](./set_toppadding/)(double) | Définisseur pour [Aspose::Words::Tables::Table::get_TopPadding](./get_toppadding/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Définisseur pour [Aspose::Words::Tables::Table::get_VerticalAnchor](./get_verticalanchor/). |
| [SetBorder](./setborder/)(Aspose::Words::BorderType, Aspose::Words::LineStyle, double, System::Drawing::Color, bool) | Définit la bordure de tableau spécifiée avec le style de ligne, la largeur et la couleur spécifiés. |
| [SetBorders](./setborders/)(Aspose::Words::LineStyle, double, System::Drawing::Color) | Définit toutes les bordures du tableau avec le style de ligne, la largeur et la couleur spécifiés. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetShading](./setshading/)(Aspose::Words::TextureIndex, System::Drawing::Color, System::Drawing::Color) | Applique l’ombrage aux valeurs spécifiées sur l’ensemble du tableau. |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [Table](./table/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initialise une nouvelle instance de la classe [Table](./). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


[Table](./) is a block-level node and can be a child of classes derived from [Story](../../aspose.words/story/) or [InlineStory](../../aspose.words/inlinestory/).

[Table](./) can contain one or more [Row](../row/) nodes.

Un tableau valide minimal doit contenir au moins une [Row](../row/).

## Exemples



Montre comment créer un tableau formaté 2x2.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Lors de la création du tableau, le constructeur de document appliquera les valeurs actuelles de ses propriétés RowFormat/CellFormat.
// à la ligne/colonne actuelle où se trouve le curseur ainsi qu'aux nouvelles lignes/colonnes créées.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Les lignes et cellules ajoutées précédemment ne sont pas affectées rétroactivement par les modifications du formatage du constructeur.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```


Montre comment créer un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Les tables contiennent des lignes, qui contiennent des cellules, qui peuvent avoir des paragraphes
// avec des éléments typiques tels que des segments, des formes, et même d'autres tables.
// Appeler la méthode "EnsureMinimum" sur une table garantira que
// la table possède au moins une ligne, une cellule et un paragraphe.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Ajoutez du texte à la première cellule de la première ligne de la table.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```


Montre comment parcourir toutes les tables du document et imprimer le contenu de chaque cellule.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Nous pouvons utiliser la méthode "ToArray" sur une collection de lignes pour la cloner dans un tableau.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Nous pouvons utiliser la méthode "ToArray" sur une collection de cellules pour la cloner dans un tableau.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```

## Voir aussi

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
