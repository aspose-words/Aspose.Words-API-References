---
title: "Класс Aspose::Words::BuildingBlocks::BuildingBlock"
linktitle: "BuildingBlock"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::BuildingBlocks::BuildingBlock. Представляет запись глоссария документа, такую как строительный блок, автотекст или запись автокоррекции. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class


Представляет элемент глоссарного документа, такой как строительный блок, автотекст или запись автокоррекции. Чтобы узнать больше, посетите статью документации [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class BuildingBlock : public Aspose::Words::CompositeNode
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения конца [BuildingBlock](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения начала [BuildingBlock](./). |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [BuildingBlock](./buildingblock/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | Инициализирует новый экземпляр этого класса. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создаёт дубликат узла. |
| [get_Behavior](./get_behavior/)() const | Указывает поведение, которое должно применяться, когда содержимое строительного блока вставляется в основной документ. |
| [get_Category](./get_category/)() const | Указывает категоризацию второго уровня для строительного блока. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| [get_Description](./get_description/)() const | Получает или задает описание, связанное с этим строительным блоком. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_FirstSection](./get_firstsection/)() | Получает первый раздел в строительном блоке. |
| [get_Gallery](./get_gallery/)() const | Указывает категоризацию первого уровня для строительного блока в целях классификации или сортировки пользовательского интерфейса. |
| [get_Guid](./get_guid/)() const | Получает или задает идентификатор (128‑битный GUID), который уникально идентифицирует этот строительный блок. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_LastSection](./get_lastsection/)() | Получает последний раздел в строительном блоке. |
| [get_Name](./get_name/)() const | Получает или задает имя этого строительного блока. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает значение [BuildingBlock](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Возвращает объект [Range](../../aspose.words/range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_Sections](./get_sections/)() | Возвращает коллекцию, представляющую все разделы в строительном блоке. |
| [get_Type](./get_type/)() const | Указывает тип строительного блока. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Возвращает первого предка указанного [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Возвращает N‑й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Обеспечивает поддержку итерации в стиле foreach по дочерним узлам этого узла. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родительского узла. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все дочерние узлы [SmartTag](../../aspose.words.markup/smarttag/) текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Выбирает список узлов, соответствующих XPath-выражению. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Выбирает первый [Node](../../aspose.words/node/), соответствующий XPath-выражению. |
| [set_Behavior](./set_behavior/)(Aspose::Words::BuildingBlocks::BuildingBlockBehavior) | Указывает поведение, которое должно применяться, когда содержимое строительного блока вставляется в основной документ. |
| [set_Category](./set_category/)(const System::String\&) | Сеттер для [Aspose::Words::BuildingBlocks::BuildingBlock::get_Category](./get_category/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Description](./set_description/)(const System::String\&) | Сеттер для [Aspose::Words::BuildingBlocks::BuildingBlock::get_Description](./get_description/). |
| [set_Gallery](./set_gallery/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery) | Сеттер для [Aspose::Words::BuildingBlocks::BuildingBlock::get_Gallery](./get_gallery/). |
| [set_Guid](./set_guid/)(System::Guid) | Сеттер для [Aspose::Words::BuildingBlocks::BuildingBlock::get_Guid](./get_guid/). |
| [set_Name](./set_name/)(const System::String\&) | Сеттер для [Aspose::Words::BuildingBlocks::BuildingBlock::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Type](./set_type/)(Aspose::Words::BuildingBlocks::BuildingBlockType) | Сеттер для [Aspose::Words::BuildingBlocks::BuildingBlock::get_Type](./get_type/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


[BuildingBlock](./) can contain only [Section](../../aspose.words/section/) nodes.

[BuildingBlock](./) can only be a child of [GlossaryDocument](../glossarydocument/).

Вы можете создавать новые строительные блоки и вставлять их в глоссарный документ. Вы можете изменять или удалять существующие строительные блоки. Вы можете копировать или перемещать строительные блоки между документами. Вы можете вставлять содержимое строительного блока в документ.

Соответствует элементам **docPart**, **docPartPr** и **docPartBody** в OOXML.

## См. также

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
