---
title: "طريقة Aspose::Words::CompositeNode::RemoveSmartTags"
linktitle: "RemoveSmartTags"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::CompositeNode::RemoveSmartTags. يزيل جميع عقد SmartTag التابعة للعقدة الحالية في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words/compositenode/removesmarttags/
---
## CompositeNode::RemoveSmartTags method


يزيل جميع عقد [SmartTag](../../../aspose.words.markup/smarttag/) التابعة للعقدة الحالية.

```cpp
void Aspose::Words::CompositeNode::RemoveSmartTags()
```


## أمثلة



يزيل جميع العلامات الذكية من العقد التابعة لعقدة مركبة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

ASSERT_EQ(8, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());

doc->RemoveSmartTags();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());
```

## انظر أيضًا

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
