---
title: Class Inline
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Inline сорт. Базовый класс для узлов строчного уровня с которыми может быть связано форматирование символов но не может иметь собственных дочерних узлов.
type: docs
weight: 3260
url: /ru/net/aspose.words/inline/
---
## Inline class

Базовый класс для узлов строчного уровня, с которыми может быть связано форматирование символов, но не может иметь собственных дочерних узлов.

Чтобы узнать больше, посетите[Логические уровни узлов в документе](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) статья документации.

```csharp
public abstract class Inline : Node
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [Font](../../aspose.words/inline/font/) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Возвращает`истинный` если этот узел может содержать другие узлы. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Возвращает`истинный` если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Возвращает`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Получает тип этого узла. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Получает родительский элемент[`Paragraph`](../paragraph/) этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/) объект, представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Получает текст этого узла и всех его дочерних элементов. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя от родителя. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

Класс, производный от`Inline` может быть ребенком[`Paragraph`](../paragraph/).

### Примеры

Показывает, как определить тип редакции встроенного узла.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Когда мы редактируем документ, в то время как опция «Отслеживать изменения», которую можно найти в разделе «Просмотр» -> Отслеживание,
// включен в Microsoft Word, вносимые нами изменения считаются исправлениями.
// При редактировании документа с помощью Aspose.Words мы можем начать отслеживать изменения,
// вызываем метод StartTrackRevisions документа и прекращаем отслеживание с помощью метода StopTrackRevisions.
// Мы можем принять изменения, чтобы включить их в документ
// или отклонить их, чтобы эффективно изменить предлагаемое изменение.
Assert.AreEqual(6, doc.Revisions.Count);

// Родительским узлом ревизии является прогон, к которому относится ревизия. Run — это встроенный узел.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Ниже приведены пять типов ревизий, которые могут пометить встроенный узел.
// 1 - «Вставка» ревизии:
// Эта редакция происходит, когда мы вставляем текст во время отслеживания изменений.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Версия "формата":
// Эта редакция происходит, когда мы меняем форматирование текста при отслеживании изменений.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - переход от ревизии:
// Когда мы выделяем текст в Microsoft Word, а затем перетаскиваем его в другое место документа
// при отслеживании изменений появляются две ревизии.
// Ревизия «переместить из» — это копия исходного текста до того, как мы его переместили.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 — «перейти на» ревизию:
// Ревизия «переместить в» — это текст, который мы переместили в новую позицию в документе.
// Ревизии «Переместить из» и «Перейти в» появляются парами для каждой выполняемой нами ревизии перемещения.
// Принятие ревизии перемещения удаляет ревизию «переместить из» и ее текст,
// и сохраняет текст из версии «перейти в».
// Отклонение ревизии перемещения, наоборот, сохраняет ревизию «перейти из» и удаляет ревизию «перейти в».
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - "Удалить" ревизию:
// Эта редакция возникает, когда мы удаляем текст во время отслеживания изменений. Когда мы удаляем такой текст,
// она останется в документе как редакция, пока мы либо не примем редакцию,
// который удалит текст навсегда или отклонит редакцию, что сохранит удаленный нами текст там, где он был.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Смотрите также

* class [Node](../node/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


