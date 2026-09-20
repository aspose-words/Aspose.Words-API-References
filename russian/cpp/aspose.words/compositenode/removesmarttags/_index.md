---
title: "Метод Aspose::Words::CompositeNode::RemoveSmartTags"
linktitle: "RemoveSmartTags"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::CompositeNode::RemoveSmartTags. Удаляет все дочерние узлы SmartTag текущего узла в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words/compositenode/removesmarttags/
---
## CompositeNode::RemoveSmartTags method


Удаляет все дочерние узлы [SmartTag](../../../aspose.words.markup/smarttag/) текущего узла.

```cpp
void Aspose::Words::CompositeNode::RemoveSmartTags()
```


## Примеры



Удаляет все смарт-теги из дочерних узлов составного узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

ASSERT_EQ(8, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());

doc->RemoveSmartTags();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());
```

## См. также

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
