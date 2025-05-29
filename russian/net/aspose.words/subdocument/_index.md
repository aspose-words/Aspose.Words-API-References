---
title: SubDocument Class
linktitle: SubDocument
articleTitle: SubDocument
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.SubDocument, эффективно управляйте внешними документами и ссылайтесь на них для бесшовной интеграции и улучшенной обработки документов.
type: docs
weight: 7020
url: /ru/net/aspose.words/subdocument/
---
## SubDocument class

Представляет собой**Поддокумент** - что является ссылкой на внешний сохраненный документ.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) документальная статья.

```csharp
public class SubDocument : Node
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Возврат`истинный` если этот узел может содержать другие узлы. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words/subdocument/nodetype/) { get; } | ВозвратSubDocument . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/)объект, представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/subdocument/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

В этой версии Aspose.Words,`SubDocument`Узлы не предоставляют публичные методы и свойства для создания или изменения поддокумента. В этой версии вы не можете инстанцировать `SubDocument` узлы или изменять существующие, за исключением их удаления.

`SubDocument` может быть только ребенком[`Paragraph`](../paragraph/).

## Примеры

Показывает, как получить доступ к поддокументу главного документа.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Этот узел служит ссылкой на внешний документ, и его содержимое недоступно.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Смотрите также

* class [Node](../node/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
