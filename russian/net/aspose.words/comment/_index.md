---
title: Class Comment
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Comment сорт. Представляет контейнер для текста комментария.
type: docs
weight: 230
url: /ru/net/aspose.words/comment/
---
## Comment class

Представляет контейнер для текста комментария.

Чтобы узнать больше, посетите[Работа с комментариями](https://docs.aspose.com/words/net/working-with-comments/) статья документации.

```csharp
public sealed class Comment : InlineStory
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Comment](comment/#constructor)(DocumentBase) | Инициализирует новый экземпляр`Comment` класс. |
| [Comment](comment/#constructor_1)(DocumentBase, string, string, DateTime) | Инициализирует новый экземпляр`Comment` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Возвращает родительский элемент`Comment` объект. Возврат`нулевой` для комментариев верхнего уровня. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Возвращает или задает имя автора комментария. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Получает дату и время создания комментария. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Получает или устанавливает флаг, указывающий, что комментарий помечен как выполненный. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого дочернего элемента узла. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Получает первый абзац статьи. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Предоставляет доступ к форматированию шрифта символа привязки этого объекта. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает`истинный` если у этого узла есть дочерние узлы. |
| [Id](../../aspose.words/comment/id/) { get; set; } | Получает идентификатор комментария. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Возвращает или устанавливает инициалы пользователя, связанного с определенным комментарием. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает`истинный` поскольку этот узел может иметь дочерние узлы. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Возвращает`истинный` если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Возвращает`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последнего дочернего узла узла. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Получает последний абзац истории. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | ВозвращаетComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Получает коллекцию абзацев, которые являются непосредственными дочерними элементами истории. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } |  |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Получает родительский элемент[`Paragraph`](../paragraph/) этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/) объект, представляющий часть документа, содержащуюся в этом узле. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Возвращает коллекцию`Comment` объекты, которые являются непосредственными дочерними элементами указанного комментария. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | ВозвращаетComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Получает коллекцию таблиц, которые являются непосредственными дочерними элементами истории. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(DocumentVisitor) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(DocumentVisitor) |  |
| [AddReply](../../aspose.words/comment/addreply/)(string, string, DateTime, string) | Добавляет ответ на этот комментарий. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Если последний дочерний элемент не является абзацем, создается и добавляется один пустой абзац. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних элементов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя от родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Удаляет все ответы на этот комментарий. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveReply](../../aspose.words/comment/removereply/)(Comment) | Удаляет указанный ответ на этот комментарий. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/)узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Выбирает первый[`Node`](../node/) которое соответствует выражению XPath. |
| [SetText](../../aspose.words/comment/settext/)(string) | Это удобный метод, позволяющий легко задать текст комментария. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

Комментарий — это аннотация, привязанная к области текста или к позиции в тексте. Комментарий может содержать произвольное количество контента на уровне блока.

Если`Comment` объект возникает сам по себе, комментарий привязывается к положению объекта`Comment` объект.

Чтобы привязать комментарий к текстовой области, необходимы три объекта:`Comment` , [`CommentRangeStart`](../commentrangestart/) и[`CommentRangeEnd`](../commentrangeend/) . Все три объекта должны иметь один и тот же .[`Id`](./id/) ценить.

`Comment` является узлом встроенного уровня и может быть только дочерним элементом[`Paragraph`](../paragraph/).

`Comment` может содержать[`Paragraph`](../paragraph/) и[`Table`](../../aspose.words.tables/table/) дочерние узлы.

### Примеры

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

 // В Microsoft Word мы можем щелкнуть правой кнопкой мыши этот комментарий в теле документа, чтобы отредактировать его или ответить на него.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Показывает, как добавить комментарий к документу и затем ответить на него.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Размещаем комментарий в узле тела документа.
// Этот комментарий появится в том месте, где находится его абзац,
// за пределами правого поля страницы и с пунктирной линией, соединяющей его с абзацем.
builder.CurrentParagraph.AppendChild(comment);

// Добавляем ответ, который будет отображаться под родительским комментарием.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Комментарии и ответы являются узлами комментариев.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Комментарии, которые не отвечают на другие комментарии, относятся к «верхнему уровню». У них нет комментариев предков.
Assert.Null(comment.Ancestor);

// Ответы содержат комментарий верхнего уровня предка.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Смотрите также

* class [InlineStory](../inlinestory/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


