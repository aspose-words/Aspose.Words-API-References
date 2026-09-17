---
title: "Aspose::Words::Node::Clone méthode"
linktitle: "Clone"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Node::Clone méthode. Crée un duplicata du nœud en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/node/clone/
---
## Node::Clone method


Crée un duplicata du nœud.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::Clone(bool isCloneChildren)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| isCloneChildren | bool | Vrai pour cloner récursivement le sous-arbre sous le nœud spécifié ; faux pour cloner uniquement le nœud lui-même. |

### ReturnValue

Le nœud cloné.
## Remarques


Cette méthode sert de constructeur de copie pour les nœuds. Le nœud cloné n'a pas de parent, mais appartient au même document que le nœud original.

Cette méthode effectue toujours une copie profonde du nœud. Le paramètre *isCloneChildren* indique s'il faut également copier tous les nœuds enfants.

## Exemples



Montre comment cloner un nœud composite.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Voici deux méthodes pour cloner un nœud composite.
// 1 -  Créez un clone d'un nœud, et créez également un clone de chacun de ses nœuds enfants.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Créez un clone d'un nœud seul, sans aucun enfant.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```

## Voir aussi

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
