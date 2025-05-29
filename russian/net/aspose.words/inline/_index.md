---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Inline, разработанный для форматирования символов в линейных узлах. Улучшите стиль вашего документа без дочерних узлов!
type: docs
weight: 3710
url: /ru/net/aspose.words/inline/
---
## Inline class

Базовый класс для узлов встроенного уровня, которые могут иметь связанное с ними форматирование символов, но не могут иметь собственных дочерних узлов.

Чтобы узнать больше, посетите[Логические уровни узлов в документе](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) документальная статья.

```csharp
public abstract class Inline : Node
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [Font](../../aspose.words/inline/font/) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Возврат`истинный` если этот узел может содержать другие узлы. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Возвращает значение true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Возвращает значение true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Возвращает значение true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Возврат`истинный` если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Возврат`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Получает тип этого узла. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Возвращает родителя[`Paragraph`](../paragraph/) этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/)объект, представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя. |
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

Класс, полученный из`Inline` может быть ребенком[`Paragraph`](../paragraph/).

## Примеры

Показывает, как определить тип ревизии встроенного узла.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Когда мы редактируем документ, используя опцию «Отслеживать изменения», которую можно найти в Обзор -> Отслеживание,
// включен в Microsoft Word, то применяемые нами изменения считаются правками.
// При редактировании документа с помощью Aspose.Words мы можем начать отслеживать изменения,
// вызов метода "StartTrackRevisions" документа и остановка отслеживания с помощью метода "StopTrackRevisions".
// Мы можем либо принять изменения, чтобы включить их в документ
// или отклонить их, чтобы эффективно изменить предлагаемое изменение.
Assert.AreEqual(6, doc.Revisions.Count);

// Родительский узел ревизии — это прогон, к которому относится ревизия. Прогон — это встроенный узел.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Ниже приведены пять типов ревизий, которые могут пометить встроенный узел.
// 1 - «Вставная» редакция:
// Эта редакция происходит, когда мы вставляем текст во время отслеживания изменений.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Изменение «формата»:
// Эта редакция происходит, когда мы меняем форматирование текста во время отслеживания изменений.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - «Переход от» пересмотра:
// Когда мы выделяем текст в Microsoft Word, а затем перетаскиваем его в другое место документа
// при отслеживании изменений появляются две ревизии.
// Редакция «перемещения» — это копия текста, который был изначально до того, как мы его переместили.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Пересмотр «перехода к»:
// Редакция «переместить в» — это текст, который мы переместили на новое место в документе.
// Ревизии «Переместить из» и «Переместить в» появляются парами для каждой выполняемой нами ревизии перемещения.
// Принятие ревизии перемещения удаляет ревизию «перемещения из» и ее текст,
// и сохраняет текст из ревизии «перейти в».
// Отклонение перенесенной версии, наоборот, сохраняет перенесенную версию и удаляет перенесенную версию.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - «удаленная» ревизия:
// Эта ревизия происходит, когда мы удаляем текст во время отслеживания изменений. Когда мы удаляем текст таким образом,
// он останется в документе как исправление, пока мы не примем исправление,
// что удалит текст навсегда или отклонит изменение, что оставит удаленный нами текст там, где он был.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Смотрите также

* class [Node](../node/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
