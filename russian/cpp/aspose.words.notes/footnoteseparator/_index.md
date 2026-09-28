---
title: "Aspose::Words::Notes::FootnoteSeparator класс"
linktitle: "FootnoteSeparator"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Notes::FootnoteSeparator класс. Представляет контейнер для разделителя сносок/конечных сносок и продолжающегося содержимого документа в C++."
type: docs
weight: 3334
url: /ru/cpp/aspose.words.notes/footnoteseparator/
---
## FootnoteSeparator class


Представляет контейнер для разделителя сноски/концевой сноски и продолжающегося содержимого документа.

```cpp
class FootnoteSeparator : public Aspose::Words::Story
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Когда реализовано в производном классе, вызывает метод VisitXXXEnd указанного посетителя документа. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Когда реализовано в производном классе, вызывает метод VisitXXXStart указанного посетителя документа. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(const System::String\&) | Укороченный метод, который создает объект [Paragraph](../../aspose.words/paragraph/) с необязательным текстом и добавляет его в конец этого объекта. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создаёт дубликат узла. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Удаляет все фигуры из текста этой истории. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_FirstParagraph](../../aspose.words/story/get_firstparagraph/)() override | Возвращает первый абзац в истории. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_LastParagraph](../../aspose.words/story/get_lastparagraph/)() override | Возвращает последний абзац в истории. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает тип этого узла. |
| [get_Paragraphs](../../aspose.words/story/get_paragraphs/)() override | Возвращает коллекцию абзацев, которые являются непосредственными дочерними элементами истории. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Возвращает объект [Range](../../aspose.words/range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_SeparatorType](./get_separatortype/)() const |  |
| [get_StoryType](../../aspose.words/story/get_storytype/)() override | Возвращает тип этой истории. |
| [get_Tables](../../aspose.words/story/get_tables/)() override | Возвращает коллекцию таблиц, которые являются непосредственными дочерними элементами истории. |
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
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


[FootnoteSeparator](./) can contain [Paragraph](../../aspose.words/paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

В документе может быть только один [FootnoteSeparator](./) каждого типа [FootnoteSeparatorType](../footnoteseparatortype/).

## Примеры



Показывает, как управлять форматом разделителя сносок.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Выровнять разделитель сносок.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## См. также

* Class [Story](../../aspose.words/story/)
* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
