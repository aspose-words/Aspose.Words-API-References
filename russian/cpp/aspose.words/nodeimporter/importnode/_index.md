---
title: "Aspose::Words::NodeImporter::ImportNode метод"
linktitle: "ImportNode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeImporter::ImportNode метод. Импортирует узел из одного документа в другой в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/nodeimporter/importnode/
---
## NodeImporter::ImportNode method


Импортирует узел из одного документа в другой.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeImporter::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Узел для импорта. |
| isImportChildren | bool | **true** для импорта всех дочерних узлов рекурсивно; иначе **false**. |

### ReturnValue

Клонированный, импортированный узел. Узел принадлежит целевому документу, но не имеет родителя.
## Примечания


Импорт узла создаёт копию исходного узла, принадлежащего импортирующему документу. Возвращённый узел не имеет родителя. Исходный узел не изменяется и не удаляется из оригинального документа.

Прежде чем узел из другого документа может быть вставлен в этот документ, его необходимо импортировать. Во время импорта свойства, специфичные для документа, такие как ссылки на стили и списки, переводятся из оригинального в импортирующий документ. После импорта узел может быть вставлен в соответствующее место документа с помощью [InsertBefore1()</see> или <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Если исходный узел уже принадлежит целевому документу, то просто создаётся глубокая копия исходного узла.

## См. также

* Class [Node](../../node/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
