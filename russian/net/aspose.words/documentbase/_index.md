---
title: Class DocumentBase
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.DocumentBase сорт. Предоставляет абстрактный базовый класс для основного документа и глоссария документа Word.
type: docs
weight: 440
url: /ru/net/aspose.words/documentbase/
---
## DocumentBase class

Предоставляет абстрактный базовый класс для основного документа и глоссария документа Word.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) статья документации.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Получает или задает форму фона документа. Возможно`нулевой` . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Получает этот экземпляр. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого дочернего элемента узла. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Предоставляет доступ к свойствам шрифтов, используемых в этом документе. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает`истинный` если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает`истинный` поскольку этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последнего дочернего узла узла. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Предоставляет доступ к форматированию списка, используемому в документе. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Вызывается, когда узел вставляется или удаляется в документе. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Получает тип этого узла. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Получает или задает цвет страницы документа. Это свойство представляет собой более простую версию[`BackgroundShape`](./backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/) объект, представляющий часть документа, содержащуюся в этом узле. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Позволяет контролировать загрузку внешних ресурсов. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Возвращает коллекцию стилей, определенных в документе. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере данных или точности форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Принимает посетителя. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(DocumentVisitor) |  |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних элементов. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode)(Node, bool) | Импортирует узел из другого документа в текущий документ. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode_1)(Node, bool, ImportFormatMode) | Импортирует узел из другого документа в текущий документ с возможностью управления форматированием. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя от родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/)узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Выбирает первый[`Node`](../node/) которое соответствует выражению XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

Aspose.Words представляет документ Word как дерево узлов.`DocumentBase` является корневым узлом a дерева, которое содержит все остальные узлы документа.

`DocumentBase` также хранит информацию по всему документу, такую как[`Styles`](./styles/) and [`Lists`](./lists/) на которые могут ссылаться узлы дерева.

### Примеры

Показывает, как инициализировать подклассы DocumentBase.

```csharp
Document doc = new Document();

Assert.AreEqual(typeof(DocumentBase), doc.GetType().BaseType);

GlossaryDocument glossaryDoc = new GlossaryDocument();
doc.GlossaryDocument = glossaryDoc;

Assert.AreEqual(typeof(DocumentBase), glossaryDoc.GetType().BaseType);
```

### Смотрите также

* class [CompositeNode](../compositenode/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


