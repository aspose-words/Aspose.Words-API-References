---
title: "Aspose::Words::CompositeNode::RemoveSmartTags‑metod"
linktitle: "RemoveSmartTags"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CompositeNode::RemoveSmartTags‑metod. Tar bort alla SmartTag‑nedärvda noder till den aktuella noden i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words/compositenode/removesmarttags/
---
## CompositeNode::RemoveSmartTags method


Tar bort alla [SmartTag](../../../aspose.words.markup/smarttag/) nedärvda noder till den aktuella noden.

```cpp
void Aspose::Words::CompositeNode::RemoveSmartTags()
```


## Exempel



Tar bort alla smarta taggar från nedärvda noder i en sammansatt nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

ASSERT_EQ(8, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());

doc->RemoveSmartTags();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());
```

## Se även

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
