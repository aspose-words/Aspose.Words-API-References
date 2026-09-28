---
title: "Класс Aspose::Words::Notes::Footnote"
linktitle: "Footnote"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Notes::Footnote. Представляет контейнер для текста сноски или концевой сноски. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.notes/footnote/
---
## Footnote class


Представляет контейнер для текста сноски или концевой сноски. Чтобы узнать больше, посетите статью документации [Working with Footnote and Endnote](https://docs.aspose.com/words/cpp/working-with-footnote-and-endnote/).

```cpp
class Footnote : public Aspose::Words::InlineStory,
                 public Aspose::Words::Revisions::ITrackableNode
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения конца сноски. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения начала сноски. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Создаёт дубликат узла. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Если последний дочерний элемент не является абзацем, создаёт и добавляет один пустой абзац. |
| [Footnote](./footnote/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Notes::FootnoteType) | Инициализирует экземпляр класса [Footnote](./). |
| [get_ActualReferenceMark](./get_actualreferencemark/)() | Получает фактический текст ссылочного знака, отображаемого в документе для этой сноски. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_FirstParagraph](../../aspose.words/inlinestory/get_firstparagraph/)() override | Возвращает первый абзац в истории. |
| [get_Font](../../aspose.words/inlinestory/get_font/)() | Предоставляет доступ к форматированию шрифта символа‑якоря этого объекта. |
| [get_FootnoteType](./get_footnotetype/)() const | Возвращает значение, указывающее, является ли это сноской или концевой сноской. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_IsAuto](./get_isauto/)() const | Содержит значение, указывающее, является ли это автоматически нумерованной сноской или сноской с пользовательским ссылочным знаком. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_IsDeleteRevision](../../aspose.words/inlinestory/get_isdeleterevision/)() | Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений. |
| [get_IsInsertRevision](../../aspose.words/inlinestory/get_isinsertrevision/)() | Возвращает true, если этот объект был вставлен в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveFromRevision](../../aspose.words/inlinestory/get_ismovefromrevision/)() | Возвращает **true**, если этот объект был перемещён (удалён) в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveToRevision](../../aspose.words/inlinestory/get_ismovetorevision/)() | Возвращает **true**, если этот объект был перемещён (вставлен) в Microsoft Word при включённом отслеживании изменений. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_LastParagraph](../../aspose.words/inlinestory/get_lastparagraph/)() override | Возвращает последний абзац в истории. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает [Footnote](../../aspose.words/nodetype/). |
| [get_Paragraphs](../../aspose.words/inlinestory/get_paragraphs/)() override | Возвращает коллекцию абзацев, которые являются непосредственными дочерними элементами истории. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_ParentParagraph](../../aspose.words/inlinestory/get_parentparagraph/)() | Получает родительский [Paragraph](../../aspose.words/paragraph/) этого узла. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Возвращает объект [Range](../../aspose.words/range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_ReferenceMark](./get_referencemark/)() const | Получает/устанавливает пользовательский ссылочный знак, используемый для этой сноски. Значение по умолчанию — **empty string**, что означает использование автонумерованных сносок. |
| [get_StoryType](./get_storytype/)() override | Возвращает [Footnotes](../../aspose.words/storytype/) или [Endnotes](../../aspose.words/storytype/). |
| [get_Tables](../../aspose.words/inlinestory/get_tables/)() override | Возвращает коллекцию таблиц, которые являются непосредственными дочерними элементами истории. |
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
| [set_IsAuto](./set_isauto/)(bool) | Сеттер для [Aspose::Words::Notes::Footnote::get_IsAuto](./get_isauto/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ReferenceMark](./set_referencemark/)(const System::String\&) | Сеттер для [Aspose::Words::Notes::Footnote::get_ReferenceMark](./get_referencemark/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


Класс [Footnote](./) используется для представления как сносок, так и концевых сносок в документе Word.

[Footnote](./) is an inline-level node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[Footnote](./) can contain [Paragraph](../../aspose.words/paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## Примеры



Показывает, как вставлять и настраивать сноски.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Добавьте текст и сослаться на него с помощью сноски. Эта сноска разместит небольшую надстрочную ссылку
// после текста, на который она ссылается, и создаст запись под основным текстом внизу страницы.
// Эта запись будет содержать маркер ссылки сноски и текст ссылки,
// которые мы передадим методу "InsertFootnote" построителя документа.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Если это свойство установлено в "true", то маркер ссылки нашей сноски
// будет её индексом среди всех сносок раздела.
// Это первая сноска, поэтому её маркер будет "1".
ASSERT_TRUE(footnote->get_IsAuto());

// Мы можем переместить построитель документа внутрь сноски, чтобы отредактировать её текст ссылки.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Мы можем задать пользовательский маркер ссылки, который сноска будет использовать вместо своего порядкового номера.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// Закладка с флагом "IsAuto", установленным в true, всё равно покажет свой реальный индекс
// даже если предыдущие закладки отображают пользовательские маркеры, поэтому маркер этой закладки будет "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```

## См. также

* Class [InlineStory](../../aspose.words/inlinestory/)
* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
