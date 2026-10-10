---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart classe"
linktitle: "StructuredDocumentTagRangeStart"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart classe. Représente le début d'une balise de document structuré à portée qui accepte du contenu multi‑sections. Voir également StructuredDocumentTagRangeEnd. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class


Représente le début d'une balise de document structuré **ranged** qui accepte du contenu multi‑sections. Voir également [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/). Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagRangeStart : public Aspose::Words::Node,
                                        public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                                        public Aspose::Words::Markup::IStructuredDocumentTag
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [AppendChild](./appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ajoute le nœud spécifié à la fin de la plage stdContent. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_Appearance](./get_appearance/)() override | Obtient ou définit l'apparence de la balise de document structuré. |
| [get_Color](./get_color/)() override | Obtient ou définit la couleur de la balise de document structuré. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_Id](./get_id/)() override | Spécifie un identifiant numérique persistant en lecture seule unique pour cette balise de document structuré. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Renvoie **true** si ce nœud peut contenir d'autres nœuds. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Spécifie si le contenu de cette balise de document structuré doit être interprété comme contenant du texte de substitution (par opposition au texte ordinaire à l'intérieur de la balise). Si la valeur est **true**, cet état sera réactivé (affichage du texte de substitution) à l'ouverture du document. |
| [get_LastChild](./get_lastchild/)() | Obtient le dernier enfant de la plage stdContent. |
| [get_Level](./get_level/)() const override | Obtient le niveau auquel le début de la plage de cette balise de document structuré se trouve dans l'arborescence du document. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | Lorsque la valeur est **true**, cette propriété empêchera un utilisateur de supprimer cette balise de document structuré. |
| [get_LockContents](./get_lockcontents/)() override | Lorsque la valeur est **true**, cette propriété empêchera un utilisateur de modifier le contenu de cette balise de document structuré. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie [StructuredDocumentTagRangeStart](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_Placeholder](./get_placeholder/)() override | Obtient le [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenant le texte de substitution qui doit être affiché lorsque le contenu de cette balise de document structuré est vide, que l'élément XML mappé associé est vide comme spécifié via l'élément [XmlMapping](./get_xmlmapping/) ou que l'élément [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) est **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Obtient ou définit le nom du [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenant le texte de substitution. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Renvoie un objet [Range](../../aspose.words/range/) qui représente la partie d'un document contenue dans ce nœud. |
| [get_RangeEnd](./get_rangeend/)() | Spécifie la fin de la plage si le [StructuredDocumentTag](../structureddocumenttag/) est une balise de document structuré à portée. Sinon, renvoie **null**. |
| [get_SdtType](./get_sdttype/)() override | Obtient le type de cette balise de document structuré. |
| [get_Tag](./get_tag/)() const override | Spécifie une balise associée au nœud de la balise de document structuré actuel. Ne peut pas être **null**. |
| [get_Title](./get_title/)() const override | Spécifie le nom convivial associé à cette balise de document structuré. Ne peut pas être **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Obtient une chaîne qui représente le XML contenu dans le nœud au format [FlatOpc](../../aspose.words/saveformat/). |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Obtient une chaîne qui représente le XML contenu dans le nœud au format [FlatOpc](../../aspose.words/saveformat/). Contrairement à la propriété [WordOpenXML](./get_wordopenxml/), cette méthode génère un document allégé qui exclut toutes les parties non liées au contenu. |
| [get_XmlMapping](./get_xmlmapping/)() override | Obtient un objet qui représente le mappage de cette plage de balise de document structuré aux données XML d'une partie XML personnalisée du document actuel. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../../aspose.words/nodetype/) spécifié. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Renvoie une collection en direct des nœuds enfants correspondant aux types spécifiés. |
| [GetEnumerator](./getenumerator/)() override | Fournit une prise en charge de l'itération de type foreach sur les nœuds enfants de ce nœud. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](./removeallchildren/)() | Supprime tous les nœuds entre ce nœud de début de plage et le nœud de fin de plage. |
| [RemoveSelfOnly](./removeselfonly/)() override | Supprime ce nœud de début de plage et les nœuds de fin de plage appropriés de la balise de document structuré, tout en conservant son contenu dans l'arborescence du document. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance](./get_appearance/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Mutateur pour [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Mutateur pour [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Définisseur pour [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContents](./get_lockcontents/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Définisseur pour [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Tag](./set_tag/)(System::String) override | Définisseur pour [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Définisseur pour [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Title](./get_title/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType) | Initialise une nouvelle instance de la classe **Structured document tag range start**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |

## Exemples



Montre comment obtenir les propriétés des balises de document structuré multi‑sections.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## Voir aussi

* Class [Node](../../aspose.words/node/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
