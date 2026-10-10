---
title: "Aspose::Words::CompositeNode::IndexOf méthode"
linktitle: "IndexOf"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::CompositeNode::IndexOf méthode. Retourne l'index du nœud enfant spécifié dans le tableau des nœuds enfants en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words/compositenode/indexof/
---
## CompositeNode::IndexOf method


Renvoie l'index du nœud enfant spécifié dans le tableau des nœuds enfants.

```cpp
int32_t Aspose::Words::CompositeNode::IndexOf(const System::SharedPtr<Aspose::Words::Node> &child)
```


## Exemples



Montre comment obtenir l'index d'un nœud enfant donné à partir de son parent.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();

// Récupérez l'index du dernier paragraphe dans le corps de la première section.
ASSERT_EQ(24, body->GetChildNodes(Aspose::Words::NodeType::Any, false)->IndexOf(body->get_LastParagraph()));
```

## Voir aussi

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
