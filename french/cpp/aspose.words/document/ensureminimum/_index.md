---
title: "Méthode Aspose::Words::Document::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::EnsureMinimum. Si le document ne contient aucune section, crée une section avec un paragraphe en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words/document/ensureminimum/
---
## Document::EnsureMinimum method


Si le document ne contient aucune section, crée une section avec un paragraphe.

```cpp
void Aspose::Words::Document::EnsureMinimum()
```


## Exemples



Montre comment garantir qu'un document contient l'ensemble minimal de nœuds requis pour modifier son contenu.
```cpp
// Un document nouvellement créé contient une Section enfant, qui comprend un corps (Body) enfant et un paragraphe (Paragraph) enfant.
// Nous pouvons modifier le contenu du corps du document en ajoutant des nœuds tels que des Run ou des formes en ligne à ce paragraphe.
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASPOSE_ASSERT_EQ(doc, nodes->idx_get(0)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(0), nodes->idx_get(1)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(1), nodes->idx_get(2)->get_ParentNode());

// Ceci est l'ensemble minimal de nœuds dont nous avons besoin pour pouvoir modifier le document.
// Nous ne pourrons plus modifier le document si nous en supprimons l'un d'eux.
doc->RemoveAllChildren();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Appelez cette méthode pour vous assurer que le document possède au moins ces trois nœuds afin de pouvoir le modifier à nouveau.
doc->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());

(System::ExplicitCast<Aspose::Words::Paragraph>(nodes->idx_get(2)))->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
