---
title: "Aspose::Words::CompositeNode::RemoveSmartTags metodu"
linktitle: "RemoveSmartTags"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CompositeNode::RemoveSmartTags metodu. C++'ta geçerli düğümün tüm SmartTag alt düğümlerini kaldırır."
type: docs
weight: 21000
url: /tr/cpp/aspose.words/compositenode/removesmarttags/
---
## CompositeNode::RemoveSmartTags method


Geçerli düğümün tüm [SmartTag](../../../aspose.words.markup/smarttag/) alt düğümlerini kaldırır.

```cpp
void Aspose::Words::CompositeNode::RemoveSmartTags()
```


## Örnekler



Bir birleşik düğümün alt düğümlerinden tüm akıllı etiketleri kaldırır.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

ASSERT_EQ(8, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());

doc->RemoveSmartTags();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());
```

## Ayrıca Bakınız

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
