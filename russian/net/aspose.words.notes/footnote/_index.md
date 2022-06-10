---
title: Footnote
second_title: Справочник по API Aspose.Words для .NET
description: Представляет контейнер для текста сноски или концевой сноски.
type: docs
weight: 3970
url: /ru/net/aspose.words.notes/footnote/
---
## Footnote class

Представляет контейнер для текста сноски или концевой сноски.

```csharp
public class Footnote : InlineStory
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Footnote](footnote)(DocumentBase, FootnoteType) | Инициализирует экземпляр класса **Footnote** . |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Получает все непосредственные дочерние узлы данного узла. |
| [Count](../../aspose.words/compositenode/count) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| virtual [Document](../../aspose.words/node/document) { get; } | Получает документ, которому принадлежит данный узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Получает первый потомок узла. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph) { get; } | Получает первый абзац истории. |
| [Font](../../aspose.words/inlinestory/font) { get; } | Предоставляет доступ к форматированию шрифта символа привязки этого объекта. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype) { get; } | Возвращает значение, указывающее, является ли это сноской или концевой сноской. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| [IsAuto](../../aspose.words.notes/footnote/isauto) { get; set; } | Содержит значение, указывающее, является ли это сноской с автоматической нумерацией или сноской с определяемой пользователем пользовательской отметкой. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | Возвращает **true** , если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | Возвращает **true** , если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Получает последний потомок узла. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Получает последний абзац истории. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype) { get; } | Возвращает **NodeType.Footnote** . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Получает набор абзацев, которые являются непосредственными дочерними элементами истории. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Извлекает родителя[`Paragraph`](../../aspose.words/paragraph)этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает объект **Range** , представляющий часть документа, содержащуюся в этом узле. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark) { get; set; } | Получает/устанавливает пользовательскую контрольную метку, которая будет использоваться для этой сноски. Значение по умолчанию: **пустая строка** (Empty), что означает автонумерацию используются сноски. |
| override [StoryType](../../aspose.words.notes/footnote/storytype) { get; } | Возвращает **StoryType.Footnotes** или **StoryType.Endnotes** . |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Получает набор таблиц, которые являются непосредственными дочерними элементами истории. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept)(DocumentVisitor) | Принимает посетителя. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Зарезервировано для системного использования. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum)() | Если последний потомок не является абзацем, создает и добавляет один пустой абзац. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype). |
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
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag)узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

Класс **Сноска** класс используется для представления как сносок, так и концевых сносок в документе Word.

**Сноска** является узлом встроенного уровня и может быть только потомком **Абзац** .

**Сноска** может содержать **Абзац** и **Таблица** дочерние узлы.

### Примеры

Показывает, как вставлять и настраивать сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Добавляем текст и ссылаемся на него сноской. Эта сноска поместит небольшой верхний индекс reference
 // пометить после текста, на который он ссылается, и создать запись под основным текстом внизу страницы.
 // Эта запись будет содержать отметку сноски и текст ссылки, 
 // который мы передадим методу "InsertFootnote" конструктора документов.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

 // Если для этого свойства установлено значение "true", то ссылка на нашу сноску mark
 // будет его индексом среди всех сносок раздела.
 // Это первая сноска, поэтому отметка будет "1".
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

// Закладка с флагом "IsAuto", установленным в true, по-прежнему будет показывать свой реальный index
 // даже если предыдущие закладки отображают пользовательские метки ссылок, метка этой закладки будет "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Смотрите также

* class [InlineStory](../../aspose.words/inlinestory)
* пространство имен [Aspose.Words.Notes](../../aspose.words.notes)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
