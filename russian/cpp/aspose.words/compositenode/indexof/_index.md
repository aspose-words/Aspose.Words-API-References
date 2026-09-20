---
title: "метод Aspose::Words::CompositeNode::IndexOf"
linktitle: "IndexOf"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::CompositeNode::IndexOf. Возвращает индекс указанного дочернего узла в массиве дочерних узлов в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words/compositenode/indexof/
---
## CompositeNode::IndexOf method


Возвращает индекс указанного дочернего узла в массиве дочерних узлов.

```cpp
int32_t Aspose::Words::CompositeNode::IndexOf(const System::SharedPtr<Aspose::Words::Node> &child)
```


## Примеры



Показывает, как получить индекс заданного дочернего узла от его родителя.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();

// Получите индекс последнего абзаца в теле первого раздела.
ASSERT_EQ(24, body->GetChildNodes(Aspose::Words::NodeType::Any, false)->IndexOf(body->get_LastParagraph()));
```

## См. также

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
