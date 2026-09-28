---
title: "Aspose::Words::Comment class"
linktitle: "Comment"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Comment class. Представляет контейнер для текста комментария. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words/comment/
---
## Comment class


Представляет контейнер для текста комментария. Чтобы узнать больше, посетите статью документации [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class Comment : public Aspose::Words::InlineStory,
                public Aspose::Words::INodeWithAnnotationId,
                public Aspose::Words::Revisions::IMoveTrackableNode
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения конца комментария. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения начала комментария. |
| [AddReply](./addreply/)(const System::String\&, const System::String\&, System::DateTime, const System::String\&) | Добавляет ответ к этому комментарию. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Создаёт дубликат узла. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Инициализирует новый экземпляр класса [Comment](./). |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) | Инициализирует новый экземпляр класса [Comment](./). |
| [EnsureMinimum](../inlinestory/ensureminimum/)() | Если последний дочерний элемент не является абзацем, создаёт и добавляет один пустой абзац. |
| [get_Ancestor](./get_ancestor/)() | Возвращает родительский объект [Comment](./). Возвращает **null** для комментариев верхнего уровня. |
| [get_Author](./get_author/)() const | Возвращает или задает имя автора комментария. |
| [get_Count](../compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| [get_DateTime](./get_datetime/)() const | Получает дату и время создания комментария. |
| [get_DateTimeUtc](./get_datetimeutc/)() | Получает дату и время UTC создания комментария. |
| virtual [get_Document](../node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_Done](./get_done/)() const | Получает или задает флаг, указывающий, что комментарий помечен как выполненный. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_FirstParagraph](../inlinestory/get_firstparagraph/)() override | Возвращает первый абзац в истории. |
| [get_Font](../inlinestory/get_font/)() | Предоставляет доступ к форматированию шрифта символа‑якоря этого объекта. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_Id](./get_id/)() const | Получает или задает идентификатор комментария. |
| [get_Initial](./get_initial/)() const | Возвращает или задает инициалы пользователя, связанного с конкретным комментарием. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_IsDeleteRevision](../inlinestory/get_isdeleterevision/)() | Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений. |
| [get_IsInsertRevision](../inlinestory/get_isinsertrevision/)() | Возвращает true, если этот объект был вставлен в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveFromRevision](../inlinestory/get_ismovefromrevision/)() | Возвращает **true**, если этот объект был перемещён (удалён) в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveToRevision](../inlinestory/get_ismovetorevision/)() | Возвращает **true**, если этот объект был перемещён (вставлен) в Microsoft Word при включённом отслеживании изменений. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_LastParagraph](../inlinestory/get_lastparagraph/)() override | Возвращает последний абзац в истории. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает [Comment](../nodetype/). |
| [get_Paragraphs](../inlinestory/get_paragraphs/)() override | Возвращает коллекцию абзацев, которые являются непосредственными дочерними элементами истории. |
| [get_ParentId](./get_parentid/)() const | Получает идентификатор родительского комментария. Значение **%-1** означает, что у комментария нет родителя. |
| [get_ParentNode](../node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_ParentParagraph](../inlinestory/get_parentparagraph/)() | Получает родительский [Paragraph](../paragraph/) этого узла. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Возвращает объект [Range](../range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_Replies](./get_replies/)() | Возвращает коллекцию объектов [Comment](./), которые являются непосредственными дочерними элементами указанного комментария. |
| [get_StoryType](./get_storytype/)() override | Возвращает [Comments](../storytype/). |
| [get_Tables](../inlinestory/get_tables/)() override | Возвращает коллекцию таблиц, которые являются непосредственными дочерними элементами истории. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Получает первого предка указанного [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Возвращает N‑й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Обеспечивает поддержку итерации в стиле foreach по дочерним узлам этого узла. |
| [GetText](../compositenode/gettext/)() override | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../node/remove/)() | Удаляет себя из родительского узла. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveAllReplies](./removeallreplies/)() | Удаляет все ответы на этот комментарий. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveReply](./removereply/)(const System::SharedPtr\<Aspose::Words::Comment\>\&) | Удаляет указанный ответ на этот комментарий. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Удаляет все дочерние узлы [SmartTag](../../aspose.words.markup/smarttag/) текущего узла. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Выбирает список узлов, соответствующих XPath-выражению. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Выбирает первый [Node](../node/), который соответствует выражению XPath. |
| [set_Author](./set_author/)(const System::String\&) | Сеттер для [Aspose::Words::Comment::get_Author](./get_author/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | Получает дату и время создания комментария. |
| [set_Done](./set_done/)(bool) | Сеттер для [Aspose::Words::Comment::get_Done](./get_done/). |
| [set_Id](./set_id/)(int32_t) | Сеттер для [Aspose::Words::Comment::get_Id](./get_id/). |
| [set_Initial](./set_initial/)(const System::String\&) | Сеттер для [Aspose::Words::Comment::get_Initial](./get_initial/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ParentId](./set_parentid/)(int32_t) | Устанавливает идентификатор родительского комментария. Значение **%-1** означает, что у комментария нет родителя. |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetText](./settext/)(const System::String\&) | Это удобный метод, позволяющий легко задать текст комментария. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


Комментарий — это аннотация, привязанная к области текста или к позиции в тексте. Комментарий может содержать произвольное количество блочного контента.

Если объект [Comment](./) используется самостоятельно, комментарий привязывается к позиции объекта [Comment](./).

Для привязки комментария к области текста требуются три объекта: [Comment](./), [CommentRangeStart](../commentrangestart/) и [CommentRangeEnd](../commentrangeend/). Все три объекта должны иметь одинаковое значение [Id](./get_id/).

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## Примеры



Показывает, как добавить комментарий в документ и затем ответить на него.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Разместите комментарий в узле тела документа.
// Этот комментарий будет отображаться в месте своего абзаца,
// вне правого поля страницы и с пунктирной линией, соединяющей его с абзацем.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Добавьте ответ, который будет отображаться под родительским комментарием.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Комментарии и ответы являются узлами типа Comment.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Комментарии, которые не являются ответами на другие комментарии, являются "верхнего уровня". У них нет предшествующих комментариев.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Ответы имеют предшествующий комментарий верхнего уровня.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```


Показывает, как добавить комментарий к абзацу.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// В Microsoft Word мы можем щёлкнуть правой кнопкой мыши этот комментарий в теле документа, чтобы отредактировать его или ответить на него.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## См. также

* Class [InlineStory](../inlinestory/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
