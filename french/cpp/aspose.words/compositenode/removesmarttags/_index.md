---
title: "Aspose::Words::CompositeNode::RemoveSmartTags méthode"
linktitle: "RemoveSmartTags"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::CompositeNode::RemoveSmartTags méthode. Supprime tous les nœuds descendants SmartTag du nœud actuel en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words/compositenode/removesmarttags/
---
## CompositeNode::RemoveSmartTags method


Supprime tous les nœuds descendants [SmartTag](../../../aspose.words.markup/smarttag/) du nœud actuel.

```cpp
void Aspose::Words::CompositeNode::RemoveSmartTags()
```


## Exemples



Supprime toutes les smart tags des nœuds descendants d'un nœud composite.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

ASSERT_EQ(8, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());

doc->RemoveSmartTags();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());
```

## Voir aussi

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
