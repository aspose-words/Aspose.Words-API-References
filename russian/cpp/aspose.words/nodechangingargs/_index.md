---
title: "Класс Aspose::Words::NodeChangingArgs"
linktitle: "NodeChangingArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::NodeChangingArgs. Предоставляет данные для методов интерфейса INodeChangingCallback. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 42000
url: /ru/cpp/aspose.words/nodechangingargs/
---
## NodeChangingArgs class


Предоставляет данные для методов интерфейса [INodeChangingCallback](../inodechangingcallback/). Чтобы узнать больше, посетите статью документации [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeChangingArgs : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Action](./get_action/)() const | Получает значение, указывающее, какой тип события изменения узла происходит. |
| [get_NewParent](./get_newparent/)() const | Получает родительский узел, который будет установлен после завершения операции. |
| [get_Node](./get_node/)() const | Получает [Node](./get_node/), который добавляется или удаляется. |
| [get_OldParent](./get_oldparent/)() const | Получает родительский узел до начала операции. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
