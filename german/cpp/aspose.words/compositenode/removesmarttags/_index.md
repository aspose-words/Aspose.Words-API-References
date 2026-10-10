---
title: "Aspose::Words::CompositeNode::RemoveSmartTags-Methode"
linktitle: "RemoveSmartTags"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CompositeNode::RemoveSmartTags-Methode. Entfernt alle SmartTag-Nachfahrenknoten des aktuellen Knotens in C++."
type: docs
weight: 21000
url: /de/cpp/aspose.words/compositenode/removesmarttags/
---
## CompositeNode::RemoveSmartTags method


Entfernt alle [SmartTag](../../../aspose.words.markup/smarttag/) Nachfahrenknoten des aktuellen Knotens.

```cpp
void Aspose::Words::CompositeNode::RemoveSmartTags()
```


## Beispiele



Entfernt alle SmartTags von Nachfahrenknoten eines zusammengesetzten Knotens.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

ASSERT_EQ(8, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());

doc->RemoveSmartTags();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());
```

## Siehe auch

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
