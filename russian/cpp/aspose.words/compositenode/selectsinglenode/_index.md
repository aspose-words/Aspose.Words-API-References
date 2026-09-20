---
title: "Метод Aspose::Words::CompositeNode::SelectSingleNode"
linktitle: "SelectSingleNode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::CompositeNode::SelectSingleNode. Выбирает первый Node, который соответствует выражению XPath в C++."
type: docs
weight: 23000
url: /ru/cpp/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode::SelectSingleNode method


Выбирает первый [Node](../../node/), который соответствует выражению XPath.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::SelectSingleNode(const System::String &xpath)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| xpath | const System::String\& | Выражение XPath. |

### ReturnValue

Первый [Node](../../node/), который соответствует запросу XPath, или **null**, если подходящий узел не найден.
## Примечания


В данный момент поддерживаются только выражения с именами элементов. Выражения, использующие имена атрибутов, не поддерживаются.

## См. также

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
