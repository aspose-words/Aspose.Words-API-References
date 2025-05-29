---
title: Comment Class
linktitle: Comment
articleTitle: Comment
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Comment, ваш основной инструмент для управления текстом комментариев в документах. Улучшите свой рабочий процесс с помощью бесшовной интеграции!
type: docs
weight: 420
url: /ru/net/aspose.words/comment/
---
## Comment class

Представляет контейнер для текста комментария.

Чтобы узнать больше, посетите[Работа с комментариями](https://docs.aspose.com/words/net/working-with-comments/) документальная статья.

```csharp
public sealed class Comment : InlineStory
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Comment](comment/#constructor)(*[DocumentBase](../documentbase/)*) | Инициализирует новый экземпляр`Comment` класс. |
| [Comment](comment/#constructor_1)(*[DocumentBase](../documentbase/), string, string, DateTime*) | Инициализирует новый экземпляр`Comment` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Возвращает родителя`Comment`объект. Возвращает`нулевой` для комментариев верхнего уровня. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Возвращает или задает имя автора комментария. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Получает дату и время создания комментария. |
| [DateTimeUtc](../../aspose.words/comment/datetimeutc/) { get; } | Получает дату и время UTC, когда был сделан комментарий. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Возвращает или задает флаг, указывающий, что комментарий помечен как выполненный. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Получает первый абзац в истории. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Предоставляет доступ к форматированию шрифта символа привязки этого объекта. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| [Id](../../aspose.words/comment/id/) { get; set; } | Получает или задает идентификатор комментария. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Возвращает или задает инициалы пользователя, связанного с определенным комментарием. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возврат`истинный` так как этот узел может иметь дочерние узлы. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Возвращает значение true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Возвращает значение true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Возврат`истинный` если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Возврат`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Получает последний абзац в истории. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | ВозвратComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Получает коллекцию абзацев, которые являются непосредственными дочерними элементами истории. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } | Получает или задает идентификатор родительского комментария. Значение`-1` означает, что у комментария нет родителя. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Возвращает родителя[`Paragraph`](../paragraph/) этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/)объект, представляющий часть документа, содержащуюся в этом узле. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Возвращает коллекцию`Comment` объекты, которые являются непосредственными потомками указанного комментария. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | ВозвратComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Получает коллекцию таблиц, которые являются непосредственными дочерними элементами истории. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя для посещения конца комментария. |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя для посещения начала комментария. |
| [AddReply](../../aspose.words/comment/addreply/)(*string, string, DateTime, string*) | Добавляет ответ на этот комментарий. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Добавляет указанный узел в конец списка дочерних узлов для данного узла. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Если последний дочерний элемент не является абзацем, создает и добавляет один пустой абзац. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля по дочерним узлам этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Добавляет указанный узел в начало списка дочерних узлов для данного узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Удаляет все ответы на этот комментарий. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Удаляет указанный дочерний узел. |
| [RemoveReply](../../aspose.words/comment/removereply/)(*Comment*) | Удаляет указанный ответ на этот комментарий. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Выбирает первый[`Node`](../node/) что соответствует выражению XPath. |
| [SetText](../../aspose.words/comment/settext/)(*string*) | Это удобный метод, позволяющий легко задать текст комментария. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

Комментарий — это аннотация, привязанная к области текста или к позиции в тексте. Комментарий может содержать произвольное количество контента на уровне блока.

Если а`Comment` объект возникает сам по себе, комментарий привязан к позиции x000d_`Comment` объект.

Для привязки комментария к области текста необходимы три объекта:`Comment` , [`CommentRangeStart`](../commentrangestart/) и[`CommentRangeEnd`](../commentrangeend/) . Все три объекта должны иметь одинаковый [`Id`](./id/) ценить.

`Comment` является узлом встроенного уровня и может быть только дочерним узлом[`Paragraph`](../paragraph/).

`Comment` может содержать[`Paragraph`](../paragraph/) и[`Table`](../../aspose.words.tables/table/) дочерние узлы.

## Примеры

Показывает, как добавить комментарий к абзацу.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // В Microsoft Word мы можем щелкнуть правой кнопкой мыши этот комментарий в тексте документа, чтобы отредактировать его или ответить на него.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Показывает, как добавить комментарий к документу, а затем ответить на него.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Разместите комментарий в узле тела документа.
// Этот комментарий будет отображаться на месте своего абзаца,
// за пределами правого поля страницы и с пунктирной линией, соединяющей его с абзацем.
builder.CurrentParagraph.AppendChild(comment);

// Добавьте ответ, который будет отображаться под родительским комментарием.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Комментарии и ответы являются узлами комментариев.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Комментарии, которые не отвечают на другие комментарии, являются "верхнего уровня". У них нет предков.
Assert.Null(comment.Ancestor);

// Ответы имеют родительский комментарий верхнего уровня.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Смотрите также

* class [InlineStory](../inlinestory/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
