---
title: Story
second_title: Справочник по API Aspose.Words для .NET
description: Базовый класс для элементов содержащих узлы блочного уровняParagraph./paragraph/ а такжеTable../aspose.words.tables/table/ .
type: docs
weight: 5810
url: /ru/net/aspose.words/story/
---
## Story class

Базовый класс для элементов, содержащих узлы блочного уровня[`Paragraph`](../paragraph/) а также[`Table`](../../aspose.words.tables/table/) .

```csharp
public abstract class Story : CompositeNode
```

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
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Получает последний абзац в истории. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Получает тип этого узла. |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Получает набор абзацев, которые являются непосредственными дочерними элементами статьи. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Получает тип этой истории. |
| [Tables](../../aspose.words/story/tables/) { get; } | Получает набор таблиц, которые являются непосредственными дочерними элементами истории. |

## Методы

| Имя | Описание |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Принимает посетителя. |
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

Говорят, что текст документа Word состоит из нескольких историй. Основной текст хранится в основной текстовой истории, представленной[`Body`](../body/) , каждый верхний и нижний колонтитулы хранятся в отдельной истории, представленной[`HeaderFooter`](../headerfooter/).

### Примеры

Показывает, как удалить все фигуры из узла.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Используйте DocumentBuilder для вставки фигуры. Это встроенная форма,
// у которого есть родительский абзац, который является дочерним узлом тела первого раздела.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Мы можем удалить все фигуры из дочерних абзацев этого тела.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Смотрите также

* class [CompositeNode](../compositenode/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
