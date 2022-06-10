---
title: Inline
second_title: Справочник по API Aspose.Words для .NET
description: Базовый класс для узлов встроенного уровня которые могут иметь связанное с ними форматирование символов но не могут иметь собственных дочерних узлов.
type: docs
weight: 3010
url: /ru/net/aspose.words/inline/
---
## Inline class

Базовый класс для узлов встроенного уровня, которые могут иметь связанное с ними форматирование символов, но не могут иметь собственных дочерних узлов.

```csharp
public abstract class Inline : Node
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| virtual [Document](../../aspose.words/node/document) { get; } | Получает документ, которому принадлежит данный узел. |
| [Font](../../aspose.words/inline/font) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Возвращает true, если этот узел может содержать другие узлы. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | Возвращает **true** , если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | Возвращает **true** , если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Получает тип этого узла. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Извлекает родителя[`Paragraph`](../paragraph)этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает объект **Range** , представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| virtual [GetText](../../aspose.words/node/gettext)() | Получает текст этого узла и всех его потомков. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

Класс, производный от **Встроенный** может быть потомком **Параграф** .

### Примеры

Показывает, как определить тип ревизии встроенного узла.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Когда мы редактируем документ, в то время как опция «Отслеживать изменения», найденная в разделе «Обзор» -> Отслеживание, 
 // включено в Microsoft Word, вносимые нами изменения считаются ревизиями.
 // При редактировании документа с помощью Aspose.Words мы можем начать отслеживать ревизии by
 // вызов метода StartTrackRevisions документа и остановка отслеживания с помощью метода StopTrackRevisions.
 // Мы можем либо принять ревизии, чтобы ассимилировать их в document
 // или отклонить их, чтобы эффективно изменить предложенное изменение.
Assert.AreEqual(6, doc.Revisions.Count);

 // Родительский узел ревизии — это прогон, к которому относится ревизия. Run — это встроенный узел.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

 // Ниже приведены пять типов ревизий, которые могут помечать встроенный узел.
 // 1 - "Вставить" ревизию: 
 // Эта ревизия возникает, когда мы вставляем текст при отслеживании изменений.
Assert.IsTrue(runs[2].IsInsertRevision);

 // 2 - Ревизия "формата": 
// Эта ревизия происходит, когда мы меняем форматирование текста при отслеживании изменений.
Assert.IsTrue(runs[2].IsFormatRevision);

 // 3 - "Переход из" ревизии:
 // Когда мы выделяем текст в Microsoft Word, а затем перетаскиваем его в другое место в документе
 // при отслеживании изменений появляются две ревизии.
 // Ревизия «переместить из» — это копия исходного текста до того, как мы его переместили.
Assert.IsTrue(runs[4].IsMoveFromRevision);

 // 4 - "Перейти к" ревизии: 
 // Редакция «переместить в» — это текст, который мы переместили на новую позицию в документе.
 // Ревизии «Переместить из» и «Переместить в» появляются парами для каждой выполняемой нами ревизии перемещения.
 // Принятие ревизии перемещения удаляет ревизию "переместить из" и ее текст, 
 // и сохраняет текст из ревизии "move to".
// Отклонение ревизии перемещения, наоборот, сохраняет ревизию "переместить из" и удаляет ревизию "переместить в".
Assert.IsTrue(runs[1].IsMoveToRevision);

 // 5 - "удалить" ревизию:
 // Эта ревизия происходит, когда мы удаляем текст при отслеживании изменений. Когда мы удаляем такой текст, 
 // он останется в документе как ревизия, пока мы не примем эту ревизию, 
 // что удалит текст навсегда или отклонит исправление, которое сохранит текст, который мы удалили, там, где он был.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Смотрите также

* class [Node](../node)
* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
