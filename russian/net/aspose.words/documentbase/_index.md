---
title: DocumentBase Class
linktitle: DocumentBase
articleTitle: DocumentBase
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.DocumentBase — необходимую основу для простого и эффективного создания и управления документами и глоссариями Word.
type: docs
weight: 650
url: /ru/net/aspose.words/documentbase/
---
## DocumentBase class

Предоставляет абстрактный базовый класс для основного документа и документа глоссария документа Word.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) документальная статья.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Получает или задает форму фона документа. Может быть`нулевой` . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Получает этот экземпляр. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Предоставляет доступ к свойствам шрифтов, используемых в этом документе. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Предоставляет доступ к разделителям сносок/концевых сносок, определенным в документе. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возврат`истинный` так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Предоставляет доступ к форматированию списка, используемому в документе. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Вызывается при вставке или удалении узла в документе. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Получает тип этого узла. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Возвращает или задает цвет страницы документа. Это свойство является более простой версией[`BackgroundShape`](./backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/)объект, представляющий часть документа, содержащуюся в этом узле. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Позволяет контролировать загрузку внешних ресурсов. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Возвращает коллекцию стилей, определенных в документе. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | При реализации в производном классе вызывает метод VisitXXXEnd указанного посетителя документа. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | При реализации в производном классе вызывает метод VisitXXXStart указанного посетителя документа. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Добавляет указанный узел в конец списка дочерних узлов для данного узла. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля по дочерним узлам этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode)(*[Node](../node/), bool*) | Импортирует узел из другого документа в текущий документ. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode_1)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Импортирует узел из другого документа в текущий документ с возможностью управления форматированием. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Добавляет указанный узел в начало списка дочерних узлов для данного узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Выбирает первый[`Node`](../node/) что соответствует выражению XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

Aspose.Words представляет документ Word в виде дерева узлов.`DocumentBase` является корневым узлом a дерева, содержащего все остальные узлы документа.

`DocumentBase` также хранит информацию по всему документу, такую как[`Styles`](./styles/) и [`Lists`](./lists/) на которые могут ссылаться узлы дерева.

## Примеры

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
