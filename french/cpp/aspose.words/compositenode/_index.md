---
title: "Aspose::Words::CompositeNode class"
linktitle: "CompositeNode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::CompositeNode class. Classe de base pour les nœuds pouvant contenir d'autres nœuds. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words/compositenode/
---
## CompositeNode class


Classe de base pour les nœuds pouvant contenir d'autres nœuds. Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class CompositeNode : public Aspose::Words::Node,
                      public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                      public Aspose::Words::INodeCollection
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepte un visiteur. |
| virtual [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Lorsqu'il est implémenté dans une classe dérivée, appelle la méthode VisitXXXEnd du visiteur de document spécifié. |
| virtual [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Lorsqu'il est implémenté dans une classe dérivée, appelle la méthode VisitXXXStart du visiteur de document spécifié. |
| [AppendChild](./appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_Count](./get_count/)() | Obtient le nombre d'enfants immédiats de ce nœud. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| virtual [get_Document](../node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_FirstChild](./get_firstchild/)() const | Obtient le premier enfant du nœud. |
| [get_HasChildNodes](./get_haschildnodes/)() | Renvoie **true** si ce nœud possède des nœuds enfants. |
| [get_IsComposite](./get_iscomposite/)() override | Renvoie **true** car ce nœud peut avoir des nœuds enfants. |
| [get_LastChild](./get_lastchild/)() const | Obtient le dernier enfant du nœud. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Obtient le type de ce nœud. |
| [get_ParentNode](../node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Renvoie un objet [Range](../range/) qui représente la partie d'un document contenue dans ce nœud. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../nodetype/) spécifié. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](./getchild/)(Aspose::Words::NodeType, int32_t, bool) | Renvoie le nième nœud enfant qui correspond au type spécifié. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié. |
| [GetEnumerator](./getenumerator/)() override | Fournit une prise en charge de l'itération de type foreach sur les nœuds enfants de ce nœud. |
| [GetText](./gettext/)() override | Obtient le texte de ce nœud et de tous ses enfants. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](./indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index du nœud enfant spécifié dans le tableau des nœuds enfants. |
| [InsertAfter](./insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](./insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PrependChild](./prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](./removeallchildren/)() | Supprime tous les nœuds enfants du nœud actuel. |
| [RemoveChild](./removechild/)(T) |  |
| [RemoveSmartTags](./removesmarttags/)() | Supprime tous les nœuds descendants [SmartTag](../../aspose.words.markup/smarttag/) du nœud actuel. |
| [SelectNodes](./selectnodes/)(const System::String\&) | Sélectionne une liste de nœuds correspondant à l'expression XPath. |
| [SelectSingleNode](./selectsinglenode/)(const System::String\&) | Sélectionne le premier [Node](../node/) qui correspond à l'expression XPath. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Définisseur pour [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Un document est représenté comme un arbre de nœuds, similaire au DOM ou à XmlDocument.

Pour plus d'informations, voir le motif de conception Composite.

La classe [CompositeNode](./) :

* Provides access to the child nodes.
* Implements Composite operations such as insert and remove children.
* Provides methods for XPath navigation.



## Exemples



Montre comment parcourir la collection de nœuds enfants d'un nœud composite.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ajoutez deux exécutions et une forme en tant que nœuds enfants au premier paragraphe de ce document.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Notez que le 'CustomNodeId' n'est pas enregistré dans un fichier de sortie et n'existe que pendant la durée de vie du nœud.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Itérez à travers la collection d'enfants immédiats du paragraphe,
// et affichez tous les runs ou formes que nous y trouvons.
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## Voir aussi

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
