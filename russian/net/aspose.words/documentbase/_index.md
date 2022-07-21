---
title: DocumentBase
second_title: Справочник по API Aspose.Words для .NET
description: Предоставляет абстрактный базовый класс для основного документа и глоссария документа Word.
type: docs
weight: 430
url: /ru/net/aspose.words/documentbase/
---
## DocumentBase class

Предоставляет абстрактный базовый класс для основного документа и глоссария документа Word.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape) { get; set; } | Получает или задает форму фона документа. Может быть нулевым. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Получает все непосредственные дочерние узлы этого узла. |
| [Count](../../aspose.words/compositenode/count) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| override [Document](../../aspose.words/documentbase/document) { get; } |  |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Получает первого потомка узла. |
| [FontInfos](../../aspose.words/documentbase/fontinfos) { get; } | Предоставляет доступ к свойствам шрифтов, используемых в этом документе. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Получает последний дочерний элемент узла. |
| [Lists](../../aspose.words/documentbase/lists) { get; } | Предоставляет доступ к форматированию списка, используемому в документе. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback) { get; set; } | Вызывается при вставке или удалении узла в документе. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Получает тип этого узла. |
| [PageColor](../../aspose.words/documentbase/pagecolor) { get; set; } | Получает или задает цвет страницы документа. Это свойство является упрощенной версией[`BackgroundShape`](./backgroundshape) . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback) { get; set; } | Позволяет контролировать загрузку внешних ресурсов. |
| [Styles](../../aspose.words/documentbase/styles) { get; } | Возвращает набор стилей, определенных в документе. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback) { get; set; } | Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Принимает посетителя. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Зарезервировано для системного использования. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Получает текст этого узла и всех его дочерних элементов. |
| [ImportNode](../../aspose.words/documentbase/importnode#importnode)(Node, bool) | Импортирует узел из другого документа в текущий документ. |
| [ImportNode](../../aspose.words/documentbase/importnode#importnode_1)(Node, bool, ImportFormatMode) | Импортирует узел из другого документа в текущий документ с возможностью управления форматированием. |
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

Aspose.Words представляет документ Word в виде дерева узлов.[`DocumentBase`](../documentbase) является корневым узлом дерева, содержащего все остальные узлы документа.

[`DocumentBase`](../documentbase) также хранит информацию о документе, такую как[`Styles`](./styles) и [`Lists`](./lists) на которые могут ссылаться узлы дерева.

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

* class [CompositeNode](../compositenode)
* пространство имен [Aspose.Words](../../aspose.words)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
