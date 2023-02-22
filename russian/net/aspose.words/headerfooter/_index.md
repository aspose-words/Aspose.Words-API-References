---
title: Class HeaderFooter
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.HeaderFooter сорт. Представляет контейнер для текста верхнего или нижнего колонтитула раздела.
type: docs
weight: 2920
url: /ru/net/aspose.words/headerfooter/
---
## HeaderFooter class

Представляет контейнер для текста верхнего или нижнего колонтитула раздела.

```csharp
public class HeaderFooter : Story
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [HeaderFooter](headerfooter/)(DocumentBase, HeaderFooterType) | Создает новый верхний или нижний колонтитул указанного типа. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Получает все непосредственные дочерние узлы этого узла. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает идентификатор пользовательского узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого потомка узла. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Получает первый абзац в истории. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype/) { get; } | Получает тип этого верхнего/нижнего колонтитула. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [IsHeader](../../aspose.words/headerfooter/isheader/) { get; } | Истинно, если это **Верхний колонтитул** объект является заголовком. |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious/) { get; set; } | Истинно, если этот верхний или нижний колонтитул связан с соответствующим верхним или нижним колонтитулом в предыдущем разделе. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Получает последний абзац в истории. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words/headerfooter/nodetype/) { get; } | Возвращает **NodeType.HeaderFooter** . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Получает набор абзацев, которые являются непосредственными дочерними элементами статьи. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentSection](../../aspose.words/headerfooter/parentsection/) { get; } | Получает родительский раздел этой истории. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Получает тип этой истории. |
| [Tables](../../aspose.words/story/tables/) { get; } | Получает набор таблиц, которые являются непосредственными дочерними элементами истории. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept/)(DocumentVisitor) | Принимает посетителя. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(string) | Быстрый метод, создающий[`Paragraph`](../paragraph/) объект с необязательным текстом и добавляет его в конец этого объекта. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Зарезервировано для системного использования. IXPathNavigable. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Удаляет все фигуры из текста этой истории. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних элементов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

**Верхний колонтитул** может содержать **Параграф** а также **Стол** дочерние узлы.

**Верхний колонтитул** является узлом уровня раздела и может быть только потомком **Раздел** . Может быть только один **Верхний колонтитул** или каждый[`HeaderFooterType`](./headerfootertype/) в **Раздел**.

Если **Раздел** не имеет **Верхний колонтитул** определенного типа или  **Верхний колонтитул** не имеет дочерних узлов, этот верхний/нижний колонтитул считается связанным с верхним/нижним колонтитулом того же типа, что и предыдущий раздел в Microsoft Word.

Когда **Верхний колонтитул** содержит по крайней мере один **Параграф**, он больше не считается связанным с предыдущим в Microsoft Word.

### Примеры

Показывает, как заменить текст в нижнем колонтитуле документа.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Показывает, как удалить все нижние колонтитулы из документа.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Перебираем каждый раздел и удаляем нижние колонтитулы всех видов.
foreach (Section section in doc.OfType<Section>())
{
    // Существует три типа нижнего и верхнего колонтитула.
    // 1 - «Первый» верхний/нижний колонтитул, который появляется только на первой странице раздела.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - «Основной» верхний/нижний колонтитул, который появляется на нечетных страницах.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - "Четный" верхний/нижний колонтитул, который появляется на четных страницах.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Показывает, как создать верхний и нижний колонтитулы.

```csharp
Document doc = new Document();

// Создаем заголовок и добавляем к нему абзац. Текст в этом абзаце
// появится в верхней части каждой страницы этого раздела над основным текстом.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Создаем нижний колонтитул и добавляем к нему абзац. Текст в этом абзаце
// появится внизу каждой страницы этого раздела, под основным текстом.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Смотрите также

* class [Story](../story/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


