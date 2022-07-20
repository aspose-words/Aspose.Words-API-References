---
title: InlineStory
second_title: Справочник по API Aspose.Words для .NET
description: Базовый класс для узлов встроенного уровня которые могут содержать абзацы и таблицы.
type: docs
weight: 3070
url: /ru/net/aspose.words/inlinestory/
---
## InlineStory class

Базовый класс для узлов встроенного уровня, которые могут содержать абзацы и таблицы.

```csharp
public abstract class InlineStory : CompositeNode
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Получает все непосредственные дочерние узлы этого узла. |
| [Count](../../aspose.words/compositenode/count) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| virtual [Document](../../aspose.words/node/document) { get; } | Получает документ, которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Получает первого потомка узла. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph) { get; } | Получает первый абзац в истории. |
| [Font](../../aspose.words/inlinestory/font) { get; } | Предоставляет доступ к форматированию шрифта символа привязки этого объекта. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Возвращает значение true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Возвращает значение true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | Возвращает **истинный** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | Возвращает **истинный** если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Получает последний дочерний элемент узла. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Получает последний абзац в истории. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Получает тип этого узла. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Получает набор абзацев, которые являются непосредственными дочерними элементами статьи. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Извлекает родителя[`Paragraph`](../paragraph) этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле. |
| abstract [StoryType](../../aspose.words/inlinestory/storytype) { get; } | Возвращает тип истории. |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Получает набор таблиц, которые являются непосредственными дочерними элементами истории. |

## Методы

| Имя | Описание |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Принимает посетителя. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Зарезервировано для системного использования. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum)() | Если последний дочерний элемент не является абзацем, создает и добавляет один пустой абзац. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Получает текст этого узла и всех его дочерних элементов. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

**встроенная история** является контейнером для узлов блочного уровня[`Paragraph`](../paragraph) а также[`Table`](../../aspose.words.tables/table).

Классы, происходящие от **встроенная история** являются узлами встроенного уровня, которые могут содержать собственный текст (абзацы и таблицы). Например, **Комментарий** node содержит текст comment и **Сноска** содержит текст сноски.

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

Показывает, как вставлять и настраивать сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем текст и ссылаемся на него сноской. Эта сноска поместит небольшую ссылку в верхнем индексе
// отметить после текста, на который он ссылается, и создать запись под основным текстом в нижней части страницы.
// Эта запись будет содержать отметку сноски и текст ссылки,
// который мы передадим методу "InsertFootnote" конструктора документов.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Если для этого свойства задано значение "true", то референтная метка нашей сноски
// будет его индексом среди всех сносок раздела.
// Это первая сноска, поэтому ссылочным знаком будет "1".
Assert.True(footnote.IsAuto);

// Мы можем переместить конструктор документа внутрь сноски, чтобы отредактировать его ссылочный текст. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Мы можем установить пользовательскую отметку, которую сноска будет использовать вместо своего порядкового номера.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Закладка с флагом "IsAuto", установленным в true, по-прежнему будет показывать свой реальный индекс
// даже если предыдущие закладки отображают пользовательские метки ссылок, метка этой закладки будет "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Смотрите также

* class [CompositeNode](../compositenode)
* пространство имен [Aspose.Words](../../aspose.words)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
