---
title: Aspose::Words::CompositeNode::RemoveSmartTags method
linktitle: RemoveSmartTags
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::RemoveSmartTags method. Removes all SmartTag descendant nodes of the current node in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words/compositenode/removesmarttags/
---
## CompositeNode::RemoveSmartTags method


Removes all [SmartTag](../../../aspose.words.markup/smarttag/) descendant nodes of the current node.

```cpp
void Aspose::Words::CompositeNode::RemoveSmartTags()
```

## Remarks

This method does not remove the content of the smart tags.
## Examples


Removes all smart tags from descendant nodes of a composite node.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Smart tags.doc"));

ASSERT_EQ(doc->GetChildNodes(NodeType::SmartTag, true)->get_Count(), 8);

doc->RemoveSmartTags();

ASSERT_EQ(doc->GetChildNodes(NodeType::SmartTag, true)->get_Count(), 0);
```
## See Also

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
