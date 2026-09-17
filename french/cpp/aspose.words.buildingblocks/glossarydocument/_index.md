---
title: "classe Aspose::Words::BuildingBlocks::GlossaryDocument"
linktitle: "GlossaryDocument"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::BuildingBlocks::GlossaryDocument. Représente l'élément racine d'un document de glossaire au sein d'un document Word. Un document de glossaire est un stockage pour AutoText, AutoCorrect et Building Blocks. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class


Représente l'élément racine d'un document de glossaire au sein d'un document Word. Un document de glossaire est un stockage pour AutoText, les entrées AutoCorrect et les Building Blocks. Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class GlossaryDocument : public Aspose::Words::DocumentBase
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter la fin du document Glossary. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur pour visiter le début du document Glossary. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/)() const | Obtient ou définit la forme d'arrière-plan du document. Peut être **null**. |
| [get_BuildingBlocks](./get_buildingblocks/)() | Renvoie une collection typée qui représente tous les blocs de construction dans le document de glossaire. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Obtient le nombre d'enfants immédiats de ce nœud. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| [get_Document](../../aspose.words/documentbase/get_document/)() const override | Obtient cette instance. |
| [get_FirstBuildingBlock](./get_firstbuildingblock/)() | Obtient le premier bloc de construction dans le document de glossaire. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Obtient le premier enfant du nœud. |
| [get_FontInfos](../../aspose.words/documentbase/get_fontinfos/)() const | Fournit l'accès aux propriétés des polices utilisées dans ce document. |
| [get_FootnoteSeparators](../../aspose.words/documentbase/get_footnoteseparators/)() const | Fournit l'accès aux séparateurs de notes de bas de page/notes de fin définis dans le document. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Renvoie **true** si ce nœud possède des nœuds enfants. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Renvoie **true** car ce nœud peut avoir des nœuds enfants. |
| [get_LastBuildingBlock](./get_lastbuildingblock/)() | Obtient le dernier bloc de construction dans le document de glossaire. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Obtient le dernier enfant du nœud. |
| [get_Lists](../../aspose.words/documentbase/get_lists/)() const | Fournit l'accès au formatage des listes utilisé dans le document. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeChangingCallback](../../aspose.words/documentbase/get_nodechangingcallback/)() | Appelé lorsqu'un nœud est inséré ou supprimé dans le document. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie la valeur [GlossaryDocument](../../aspose.words/nodetype/). |
| [get_PageColor](../../aspose.words/documentbase/get_pagecolor/)() | Obtient ou définit la couleur de page du document. Cette propriété est une version simplifiée de [BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Renvoie un objet [Range](../../aspose.words/range/) qui représente la partie d'un document contenue dans ce nœud. |
| [get_ResourceLoadingCallback](../../aspose.words/documentbase/get_resourceloadingcallback/)() const | Permet de contrôler la façon dont les ressources externes sont chargées. |
| [get_Styles](../../aspose.words/documentbase/get_styles/)() const | Renvoie une collection de styles définis dans le document. |
| [get_WarningCallback](../../aspose.words/documentbase/get_warningcallback/)() const | Appelé pendant diverses procédures de traitement de document lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../../aspose.words/nodetype/) spécifié. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetBuildingBlock](./getbuildingblock/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery, const System::String\&, const System::String\&) | Trouve un bloc de construction en utilisant la galerie, la catégorie et le nom spécifiés. |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Renvoie le nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Fournit une prise en charge de l'itération de type foreach sur les nœuds enfants de ce nœud. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Obtient le texte de ce nœud et de tous ses enfants. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importe un nœud d'un autre document vers le document actuel. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage. |
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
| [set_BackgroundShape](../../aspose.words/documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Mutateur pour [Aspose::Words::DocumentBase::get_BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Mutateur pour [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../../aspose.words/documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Appelé lorsqu'un nœud est inséré ou supprimé dans le document. |
| [set_PageColor](../../aspose.words/documentbase/set_pagecolor/)(System::Drawing::Color) | Mutateur pour [Aspose::Words::DocumentBase::get_PageColor](../../aspose.words/documentbase/get_pagecolor/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](../../aspose.words/documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Permet de contrôler la façon dont les ressources externes sont chargées. |
| [set_WarningCallback](../../aspose.words/documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Mutateur pour [Aspose::Words::DocumentBase::get_WarningCallback](../../aspose.words/documentbase/get_warningcallback/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Certains documents, généralement des modèles, peuvent contenir des entrées AutoText, AutoCorrect et/ou Building Blocks (également appelés *entrées de document de glossaire*, *parties de document* ou *blocs de construction*).

Pour accéder aux blocs de construction, vous devez charger un document dans un objet [Document](../../aspose.words/document/). Les blocs de construction seront disponibles via la propriété [GlossaryDocument](../../aspose.words/document/get_glossarydocument/).

[GlossaryDocument](./) can contain any number of [BuildingBlock](../buildingblock/) objects. Each [BuildingBlock](../buildingblock/) represents one document part.

Correspond aux éléments **glossaryDocument** et **docParts** dans OOXML.

## Voir aussi

* Class [DocumentBase](../../aspose.words/documentbase/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
