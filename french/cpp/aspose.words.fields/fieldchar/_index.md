---
title: "Classe Aspose::Words::Fields::FieldChar"
linktitle: "FieldChar"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Fields::FieldChar. Classe de base pour les nœuds qui représentent des caractères de champ dans un document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words.fields/fieldchar/
---
## FieldChar class


Classe de base pour les nœuds qui représentent les caractères de champ dans un document. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldChar : public Aspose::Words::SpecialChar
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](../../aspose.words/specialchar/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_FieldType](./get_fieldtype/)() const | Renvoie le type du champ. |
| [get_Font](../../aspose.words/inline/get_font/)() | Fournit l'accès au format de police de cet objet. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Renvoie **true** si ce nœud peut contenir d'autres nœuds. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsDirty](./get_isdirty/)() const | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Renvoie vrai si le format de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsLocked](./get_islocked/)() const | Obtient ou définit si le champ parent est verrouillé (ne doit pas recalculer son résultat). |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Renvoie **true** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Renvoie **true** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](../../aspose.words/specialchar/get_nodetype/)() const override | Renvoie [SpecialChar](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Récupère le [Paragraph](../../aspose.words/paragraph/) parent de ce nœud. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Renvoie un objet [Range](../../aspose.words/range/) qui représente la partie d'un document contenue dans ce nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../../aspose.words/nodetype/) spécifié. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetField](./getfield/)() | Renvoie un champ pour le caractère de champ. |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Obtient le caractère spécial que ce nœud représente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Mutateur pour [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsDirty](./set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::FieldChar::get_IsDirty](./get_isdirty/). |
| [set_IsLocked](./set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::FieldChar::get_IsLocked](./get_islocked/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Un champ complet dans un document Microsoft Word est une structure complexe composée d'un caractère de début de champ, du code du champ, d'un caractère séparateur, du résultat du champ et d'un caractère de fin de champ. Certains champs ne contiennent que le caractère de début, le code du champ et le caractère de fin.

Pour insérer facilement un nouveau champ dans un document, utilisez la méthode [InsertField()](../).

## Exemples



Montre comment travailler avec un nœud [FieldStart](../fieldstart/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

System::SharedPtr<Aspose::Words::Fields::FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// Récupérez l'objet façade qui représente le champ dans le document.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Mettez à jour le champ pour afficher la date actuelle.
field->Update();
```

## Voir aussi

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
