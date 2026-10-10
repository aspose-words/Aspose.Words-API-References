---
title: "Classe Aspose::Words::Markup::StructuredDocumentTag"
linktitle: "StructuredDocumentTag"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Markup::StructuredDocumentTag. Représente une balise de document structuré (SDT ou contrôle de contenu) dans un document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class


Représente une balise de document structuré (SDT ou contrôle de contenu) dans un document. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTag : public Aspose::Words::CompositeNode,
                              public Aspose::Words::Markup::IMarkupNode,
                              public Aspose::Words::Revisions::ITrackableNode,
                              public Aspose::Words::IRunAttrSource,
                              public Aspose::Words::Markup::IStructuredDocumentTag
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter la fin du [StructuredDocumentTag](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter le début du [StructuredDocumentTag](./). |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](./clear/)() | Efface le contenu de cette balise de document structuré et affiche un espace réservé s'il est défini. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_Appearance](./get_appearance/)() override | Obtient/Définit l'apparence d'une balise de document structuré. |
| [get_BuildingBlockCategory](./get_buildingblockcategory/)() | Spécifie la catégorie du bloc de construction pour ce nœud **SDT**. Ne peut pas être **null**. |
| [get_BuildingBlockGallery](./get_buildingblockgallery/)() | Spécifie le type du bloc de construction pour ce **SDT**. Ne peut pas être **null**. |
| [get_CalendarType](./get_calendartype/)() | Spécifie le type de calendrier pour ce **SDT**. La valeur par défaut est [Default](../sdtcalendartype/) |
| [get_Checked](./get_checked/)() | Obtient/Définit l'état actuel de la case à cocher **SDT**. La valeur par défaut de cette propriété est **false**. |
| [get_Color](./get_color/)() override | Obtient ou définit la couleur de la balise de document structuré. |
| [get_ContentsFont](./get_contentsfont/)() | Formatage [Font](../../aspose.words/font/) qui sera appliqué au texte saisi dans **SDT**. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Obtient le nombre d'enfants immédiats de ce nœud. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| [get_DateDisplayFormat](./get_datedisplayformat/)() | Chaîne qui représente le format dans lequel les dates sont affichées. |
| [get_DateDisplayLocale](./get_datedisplaylocale/)() | Permet de définir/obtenir le format linguistique pour la date affichée dans ce **SDT**. |
| [get_DateStorageFormat](./get_datestorageformat/)() | Obtient/Définit le format dans lequel la date d'un SDT de type date est stockée lorsque le **SDT** est lié à un nœud XML dans le magasin de données du document. La valeur par défaut est [DateTime](../sdtdatestorageformat/) |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_EndCharacterFont](./get_endcharacterfont/)() | Formatage [Font](../../aspose.words/font/) qui sera appliqué au dernier caractère du texte saisi dans **SDT**. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Obtient le premier enfant du nœud. |
| [get_FullDate](./get_fulldate/)() | Spécifie la date et l'heure complètes saisies en dernier dans ce **SDT**. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Renvoie **true** si ce nœud possède des nœuds enfants. |
| [get_Id](./get_id/)() override | Spécifie un identifiant numérique persistant en lecture seule unique pour ce **SDT**. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Renvoie **true** car ce nœud peut avoir des nœuds enfants. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Spécifie si le contenu de ce **SDT** doit être interprété comme contenant du texte d'espace réservé (par opposition au texte ordinaire à l'intérieur du SDT). si la valeur est **true**, cet état sera repris (affichage du texte d'espace réservé) à l'ouverture de ce document. |
| [get_IsTemporary](./get_istemporary/)() const | Spécifie si ce **SDT** doit être supprimé du document WordProcessingML lorsque son contenu est modifié. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Obtient le dernier enfant du nœud. |
| [get_Level](./get_level/)() const override | Obtient le niveau auquel ce **SDT** apparaît dans l'arborescence du document. |
| [get_ListItems](./get_listitems/)() | Obtient [SdtListItemCollection](../sdtlistitemcollection/) associé à ce **SDT**. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | Lorsqu'elle est **true**, cette propriété empêchera un utilisateur de supprimer ce **SDT**. |
| [get_LockContents](./get_lockcontents/)() override | Lorsqu'elle est **true**, cette propriété empêchera un utilisateur de modifier le contenu de ce **SDT**. |
| [get_Multiline](./get_multiline/)() | Spécifie si ce **SDT** autorise plusieurs lignes de texte. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie [StructuredDocumentTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_Placeholder](./get_placeholder/)() override | Obtient le [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenant le texte de l'espace réservé qui doit être affiché lorsque le contenu de l'exécution de ce SDT est vide, que l'élément XML mappé associé est vide comme spécifié via l'élément [XmlMapping](./get_xmlmapping/) ou que l'élément [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) est **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Obtient ou définit le nom du [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenant le texte de substitution. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Renvoie un objet [Range](../../aspose.words/range/) qui représente la partie d'un document contenue dans ce nœud. |
| [get_SdtType](./get_sdttype/)() override | Obtient le type de cette **Structured document tag**. |
| [get_Style](./get_style/)() | Obtient ou définit le [Style](../../aspose.words/style/) du tag de document structuré. |
| [get_StyleName](./get_stylename/)() | Obtient ou définit le nom du style appliqué au tag de document structuré. |
| [get_Tag](./get_tag/)() const override | Spécifie une balise associée au nœud SDT actuel. Ne peut pas être **null**. |
| [get_Title](./get_title/)() const override | Spécifie le nom convivial associé à ce **SDT**. Ne peut pas être **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Obtient une chaîne qui représente le XML contenu dans le nœud au format [FlatOpc](../../aspose.words/saveformat/). |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Obtient une chaîne qui représente le XML contenu dans le nœud au format [FlatOpc](../../aspose.words/saveformat/). Contrairement à la propriété [WordOpenXML](./get_wordopenxml/), cette méthode génère un document allégé qui exclut toutes les parties non liées au contenu. |
| [get_XmlMapping](./get_xmlmapping/)() override | Obtient un objet qui représente le mappage de cette balise de document structuré aux données XML dans une partie XML personnalisée du document actuel. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../../aspose.words/nodetype/) spécifié. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Renvoie le nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié. |
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
| [RemoveSelfOnly](./removeselfonly/)() override | Supprime uniquement ce nœud SDT lui‑-même, mais conserve son contenu dans l'arborescence du document. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Supprime tous les nœuds descendants [SmartTag](../smarttag/) du nœud actuel. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Sélectionne le premier [Node](../../aspose.words/node/) qui correspond à l'expression XPath. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_Appearance](./get_appearance/). |
| [set_BuildingBlockCategory](./set_buildingblockcategory/)(const System::String\&) | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory](./get_buildingblockcategory/). |
| [set_BuildingBlockGallery](./set_buildingblockgallery/)(const System::String\&) | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery](./get_buildingblockgallery/). |
| [set_CalendarType](./set_calendartype/)(Aspose::Words::Markup::SdtCalendarType) | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType](./get_calendartype/). |
| [set_Checked](./set_checked/)(bool) | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_Checked](./get_checked/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Mutateur pour [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DateDisplayFormat](./set_datedisplayformat/)(const System::String\&) | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayFormat](./get_datedisplayformat/). |
| [set_DateDisplayLocale](./set_datedisplaylocale/)(int32_t) | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale](./get_datedisplaylocale/). |
| [set_DateStorageFormat](./set_datestorageformat/)(Aspose::Words::Markup::SdtDateStorageFormat) | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat](./get_datestorageformat/). |
| [set_FullDate](./set_fulldate/)(System::DateTime) | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_FullDate](./get_fulldate/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_IsTemporary](./set_istemporary/)(bool) | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary](./get_istemporary/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| [set_Multiline](./set_multiline/)(bool) | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_Multiline](./get_multiline/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Définisseur pour [Aspose::Words::Markup::StructuredDocumentTag::get_Style](./get_style/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Définisseur pour [Aspose::Words::Markup::StructuredDocumentTag::get_StyleName](./get_stylename/). |
| [set_Tag](./set_tag/)(System::String) override | Définisseur pour [Aspose::Words::Markup::StructuredDocumentTag::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Définisseur pour [Aspose::Words::Markup::StructuredDocumentTag::get_Title](./get_title/). |
| [SetCheckedSymbol](./setcheckedsymbol/)(int32_t, const System::String\&) | Définit le symbole utilisé pour représenter l'état coché d'un contrôle de contenu case à cocher. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetUncheckedSymbol](./setuncheckedsymbol/)(int32_t, const System::String\&) | Définit le symbole utilisé pour représenter l'état décoché d'un contrôle de contenu case à cocher. |
| [StructuredDocumentTag](./structureddocumenttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType, Aspose::Words::Markup::MarkupLevel) | Initialise une nouvelle instance de la classe **Structured document tag**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Les balises de document structuré (SDT) permettent d'intégrer des sémantiques définies par le client ainsi que leur comportement et leur apparence dans un document.

Dans cette version, Aspose.Words fournit un certain nombre de méthodes et propriétés publiques pour manipuler le comportement et le contenu de [StructuredDocumentTag](./). Le mappage des nœuds SDT vers des packages XML personnalisés dans un document peut être effectué en utilisant la propriété [XmlMapping](./get_xmlmapping/).

[StructuredDocumentTag](./) can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [Body](../../aspose.words/body/), [HeaderFooter](../../aspose.words/headerfooter/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/) or a [Shape](../../aspose.words.drawing/shape/) node.
* Row-level - Among rows in a table, as a child of a [Table](../../aspose.words.tables/table/) node.
* Cell-level - Among cells in a table row, as a child of a [Row](../../aspose.words.tables/row/) node.
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../aspose.words/paragraph/).
* Nested inside another [StructuredDocumentTag](./).



## Exemples



Montre comment travailler avec les styles pour les éléments de contrôle de contenu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ci-dessous deux façons d'appliquer un style du document à une balise de document structuré.
// 1 -  Appliquer un objet de style provenant de la collection de styles du document :
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Référencer un style dans le document par son nom :
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```

## Voir aussi

* Class [CompositeNode](../../aspose.words/compositenode/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
