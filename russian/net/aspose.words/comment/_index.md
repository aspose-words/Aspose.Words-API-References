---
title: Comment
second_title: Справочник по API Aspose.Words для .NET
description: Представляет контейнер для текста комментария.
type: docs
weight: 220
url: /ru/net/aspose.words/comment/
---
## Comment class

Представляет контейнер для текста комментария.

```csharp
public sealed class Comment : InlineStory
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Comment](comment#constructor)(DocumentBase) | Инициализирует новый экземпляр класса **Комментарий** . |
| [Comment](comment#constructor_1)(DocumentBase, string, string, DateTime) | Инициализирует новый экземпляр класса **Комментарий** . |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor) { get; } | Возвращает родительский объект Comment. Возвращает null для комментариев верхнего уровня. |
| [Author](../../aspose.words/comment/author) { get; set; } | Возвращает или устанавливает имя автора комментария. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Получает все непосредственные дочерние узлы данного узла. |
| [Count](../../aspose.words/compositenode/count) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| [DateTime](../../aspose.words/comment/datetime) { get; set; } | Получает дату и время, когда был сделан комментарий. |
| virtual [Document](../../aspose.words/node/document) { get; } | Получает документ, которому принадлежит данный узел. |
| [Done](../../aspose.words/comment/done) { get; set; } | Получает или устанавливает флаг, указывающий, что комментарий помечен как выполненный. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Получает первый потомок узла. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph) { get; } | Получает первый абзац истории. |
| [Font](../../aspose.words/inlinestory/font) { get; } | Предоставляет доступ к форматированию шрифта символа привязки этого объекта. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| [Id](../../aspose.words/comment/id) { get; } | Получает идентификатор комментария. |
| [Initial](../../aspose.words/comment/initial) { get; set; } | Возвращает или устанавливает инициалы пользователя, связанные с конкретным комментарием. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | Возвращает **true** , если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | Возвращает **true** , если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Получает последний потомок узла. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Получает последний абзац истории. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words/comment/nodetype) { get; } | Возвращает **NodeType.Comment** . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Получает набор абзацев, которые являются непосредственными дочерними элементами истории. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Извлекает родителя[`Paragraph`](../paragraph)этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает объект **Range** , представляющий часть документа, содержащуюся в этом узле. |
| [Replies](../../aspose.words/comment/replies) { get; } | Возвращает коллекцию объектов[`Comment`](../comment), которые являются непосредственными дочерними элементами указанного комментария. |
| override [StoryType](../../aspose.words/comment/storytype) { get; } | Возвращает **StoryType.Comments** . |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Получает набор таблиц, которые являются непосредственными дочерними элементами истории. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept)(DocumentVisitor) | Принимает посетителя. |
| [AddReply](../../aspose.words/comment/addreply)(string, string, DateTime, string) | Добавляет ответ на этот комментарий. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Зарезервировано для системного использования. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum)() | Если последний потомок не является абзацем, создает и добавляет один пустой абзац. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Получает текст этого узла и всех его потомков. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Вставляет указанный узел сразу после указанного опорного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies)() | Удаляет все ответы на этот комментарий. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Удаляет указанный дочерний узел. |
| [RemoveReply](../../aspose.words/comment/removereply)(Comment) | Удаляет указанный ответ на этот комментарий. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag)узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [SetText](../../aspose.words/comment/settext)(string) | Это удобный метод, который позволяет легко установить текст комментария. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

Комментарий — это аннотация, привязанная к области текста или позиции в тексте. . Комментарий может содержать произвольное количество блочного контента.

Если объект[`Comment`](../comment)возникает сам по себе, комментарий привязывается к позиция объекта[`Comment`](../comment).

Для привязки комментария к области текста требуются три объекта:[`Comment`](../comment), [`CommentRangeStart`](../commentrangestart)и[`CommentRangeEnd`](../commentrangeend). Все три объекта должны иметь одно и то же значение [`Id`](./id).

[`Comment`](../comment)является узлом встроенного уровня и может быть только потомком[`Paragraph`](../paragraph).

[`Comment`](../comment)может содержать[`Paragraph`](../paragraph)и[`Table`](../../aspose.words.tables/table)дочерние узлы.

### Примеры

Показывает, как добавить комментарий к абзацу.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

 // Разместите комментарий в узле тела документа.
 // Этот комментарий будет отображаться в месте своего абзаца, 
 // за пределами правого поля страницы и с пунктирной линией, соединяющей его с абзацем.
builder.CurrentParagraph.AppendChild(comment);

 // Добавляем ответ, который будет отображаться под родительским комментарием.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

 // Комментарии и ответы являются узлами комментариев.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

 // Комментарии, которые не отвечают на другие комментарии, относятся к "верхнему уровню". У них нет комментариев предков.
Assert.Null(comment.Ancestor);

 // Ответы имеют родительский комментарий верхнего уровня.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

Показывает, как добавить комментарий к документу, а затем ответить на него.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

 // Разместите комментарий в узле тела документа.
 // Этот комментарий будет отображаться в месте своего абзаца, 
 // за пределами правого поля страницы и с пунктирной линией, соединяющей его с абзацем.
builder.CurrentParagraph.AppendChild(comment);

 // Добавляем ответ, который будет отображаться под родительским комментарием.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

 // Комментарии и ответы являются узлами комментариев.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

 // Комментарии, которые не отвечают на другие комментарии, относятся к "верхнему уровню". У них нет комментариев предков.
Assert.Null(comment.Ancestor);

 // Ответы имеют родительский комментарий верхнего уровня.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Смотрите также

* class [InlineStory](../inlinestory)
* пространство имен [Aspose.Words](../../aspose.words)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
