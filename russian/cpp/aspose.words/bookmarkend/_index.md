---
title: "класс Aspose::Words::BookmarkEnd"
linktitle: "BookmarkEnd"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::BookmarkEnd. Представляет конец закладки в документе Word. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/bookmarkend/
---
## BookmarkEnd class


Представляет конец закладки в документе Word. Чтобы узнать больше, посетите статью документации [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarkEnd : public Aspose::Words::Node,
                    public Aspose::Words::IBookmarkNode,
                    public Aspose::Words::IDisplaceableByCustomXml
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [BookmarkEnd](./bookmarkend/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | Инициализирует новый экземпляр класса [BookmarkEnd](./). |
| [Clone](../node/clone/)(bool) | Создаёт дубликат узла. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| virtual [get_Document](../node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Возвращает **true**, если этот узел может содержать другие узлы. |
| [get_Name](./get_name/)() override | Получает имя закладки. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает [BookmarkEnd](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Возвращает объект [Range](../range/), представляющий часть документа, содержащуюся в этом узле. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Получает первого предка указанного [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../node/remove/)() | Удаляет себя из родительского узла. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_Name](./set_name/)(System::String) override | Устанавливает имя закладки. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


Полная закладка в документе Word состоит из [BookmarkStart](../bookmarkstart/) и соответствующего [BookmarkEnd](./) с тем же именем закладки.

[BookmarkStart](../bookmarkstart/) and [BookmarkEnd](./) are just markers inside a document that specify where the bookmark starts and ends.

Используйте класс [Bookmark](../bookmark/) как "фасад" для работы с закладкой как с единым объектом.
## См. также

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
