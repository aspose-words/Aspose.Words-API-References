---
title: "Класс Aspose::Words::BuildingBlocks::BuildingBlockCollection"
linktitle: "BuildingBlockCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::BuildingBlocks::BuildingBlockCollection. Коллекция объектов BuildingBlock в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class


Коллекция объектов [BuildingBlock](../buildingblock/) в документе. Чтобы узнать больше, посетите статью документации [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class BuildingBlockCollection : public Aspose::Words::NodeCollection
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Добавляет узел в конец коллекции. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Определяет, находится ли узел в коллекции. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Получает количество узлов в коллекции. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Предоставляет простую итерацию в стиле "foreach" по коллекции узлов. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает строительный блок по указанному индексу. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает нулевой индекс указанного узла. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Вставляет узел в коллекцию по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Удаляет узел по указанному индексу из коллекции и из документа. |
| [ToArray](./toarray/)() | Копирует все строительные блоки из коллекции в новый массив строительных блоков. |
| static [Type](./type/)() |  |
## Примечания


Вы не создаёте экземпляры этого класса напрямую. Чтобы получить доступ к коллекции строительных блоков, используйте свойство [BuildingBlocks](../glossarydocument/get_buildingblocks/).

## См. также

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
