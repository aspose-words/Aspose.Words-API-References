---
title: "classe Aspose::Words::DocumentBase"
linktitle: "DocumentBase"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::DocumentBase. Fournit la classe de base abstraite pour un document principal et un document de glossaire d’un document Word. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words/documentbase/
---
## DocumentBase class


Fournit la classe de base abstraite pour le document principal et le document de glossaire d'un document Word. Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class DocumentBase : public Aspose::Words::CompositeNode
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepte un visiteur. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Lorsqu'il est implémenté dans une classe dérivée, appelle la méthode VisitXXXEnd du visiteur de document spécifié. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Lorsqu'il est implémenté dans une classe dérivée, appelle la méthode VisitXXXStart du visiteur de document spécifié. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_BackgroundShape](./get_backgroundshape/)() const | Obtient ou définit la forme d'arrière-plan du document. Peut être **null**. |
| [get_Count](../compositenode/get_count/)() | Obtient le nombre d'enfants immédiats de ce nœud. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| [get_Document](./get_document/)() const override | Obtient cette instance. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Obtient le premier enfant du nœud. |
| [get_FontInfos](./get_fontinfos/)() const | Fournit l'accès aux propriétés des polices utilisées dans ce document. |
| [get_FootnoteSeparators](./get_footnoteseparators/)() const | Fournit l'accès aux séparateurs de notes de bas de page/notes de fin définis dans le document. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Renvoie **true** si ce nœud possède des nœuds enfants. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Renvoie **true** car ce nœud peut avoir des nœuds enfants. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Obtient le dernier enfant du nœud. |
| [get_Lists](./get_lists/)() const | Fournit l'accès au formatage des listes utilisé dans le document. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeChangingCallback](./get_nodechangingcallback/)() | Appelé lorsqu'un nœud est inséré ou supprimé dans le document. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Obtient le type de ce nœud. |
| [get_PageColor](./get_pagecolor/)() | Obtient ou définit la couleur de page du document. Cette propriété est une version simplifiée de [BackgroundShape](./get_backgroundshape/). |
| [get_ParentNode](../node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Renvoie un objet [Range](../range/) qui représente la partie d'un document contenue dans ce nœud. |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Permet de contrôler la façon dont les ressources externes sont chargées. |
| [get_Styles](./get_styles/)() const | Renvoie une collection de styles définis dans le document. |
| [get_WarningCallback](./get_warningcallback/)() const | Appelé pendant diverses procédures de traitement de document lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../nodetype/) spécifié. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Renvoie le nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Fournit une prise en charge de l'itération de type foreach sur les nœuds enfants de ce nœud. |
| [GetText](../compositenode/gettext/)() override | Obtient le texte de ce nœud et de tous ses enfants. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importe un nœud d'un autre document vers le document actuel. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index du nœud enfant spécifié dans le tableau des nœuds enfants. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Supprime tous les nœuds descendants [SmartTag](../../aspose.words.markup/smarttag/) du nœud actuel. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Sélectionne le premier [Node](../node/) qui correspond à l'expression XPath. |
| [set_BackgroundShape](./set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Définisseur pour [Aspose::Words::DocumentBase::get_BackgroundShape](./get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Définisseur pour [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](./set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Appelé lorsqu'un nœud est inséré ou supprimé dans le document. |
| [set_PageColor](./set_pagecolor/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::DocumentBase::get_PageColor](./get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Permet de contrôler la façon dont les ressources externes sont chargées. |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Définisseur pour [Aspose::Words::DocumentBase::get_WarningCallback](./get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Aspose.Words représente un document Word sous forme d’un arbre de nœuds. [DocumentBase](./) est un nœud racine de l’arbre qui contient tous les autres nœuds du document.

[DocumentBase](./) also stores document-wide information such as [Styles](./get_styles/) and [Lists](./get_lists/) that the tree nodes might refer to.

## Exemples



Montre comment initialiser les sous‑classes de [DocumentBase](./).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(doc).get_BaseType());

auto glossaryDoc = System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>();
doc->set_GlossaryDocument(glossaryDoc);

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(glossaryDoc).get_BaseType());
```

## Voir aussi

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
