---
title: "Aspose::Words::NodeList::ToArray метод"
linktitle: "ToArray"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeList::ToArray метод. Копирует все узлы из коллекции в новый массив узлов в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/nodelist/toarray/
---
## NodeList::ToArray method


Копирует все узлы из коллекции в новый массив узлов.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Node>> Aspose::Words::NodeList::ToArray() const
```


### ReturnValue

Массив узлов.
## Примечания


Не следует добавлять/удалять узлы во время итерации по коллекции узлов, так как это делает итератор недействительным и требует обновления для живых коллекций.

Чтобы иметь возможность добавлять/удалять узлы во время итерации, используйте этот метод для копирования узлов в массив фиксированного размера, а затем итерируйтесь по массиву.

## См. также

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
