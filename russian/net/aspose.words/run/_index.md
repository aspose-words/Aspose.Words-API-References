---
title: Run
second_title: Справочник по API Aspose.Words для .NET
description: Представляет серию символов с одинаковым форматированием шрифта.
type: docs
weight: 4510
url: /ru/net/aspose.words/run/
---
## Run class

Представляет серию символов с одинаковым форматированием шрифта.

```csharp
public class Run : Inline
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Run](run#constructor)(DocumentBase) | Инициализирует новый экземпляр класса **Run** . |
| [Run](run#constructor_1)(DocumentBase, string) | Инициализирует новый экземпляр класса **Run** . |

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
| override [NodeType](../../aspose.words/run/nodetype) { get; } | Возвращает **NodeType.Run** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Извлекает родителя[`Paragraph`](../paragraph)этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает объект **Range** , представляющий часть документа, содержащуюся в этом узле. |
| [Text](../../aspose.words/run/text) { get; set; } | Получает или задает текст выполнения. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/run/accept)(DocumentVisitor) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| override [GetText](../../aspose.words/run/gettext)() | Получает текст выполнения. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

Весь текст документа хранится в виде строк текста.

**Выполнить** может быть только потомком **Параграф** или встроенный **StructuredDocumentTag** .

### Примеры

Показывает, как форматировать фрагмент текста, используя его свойство шрифта.

```csharp
Document doc = new Document();

 // Пустой документ по умолчанию имеет один абзац.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

 // Составные узлы, такие как наш абзац, могут содержать другие составные и встроенные узлы в качестве дочерних элементов.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

 // Создаем еще три узла запуска.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

 // Тело документа не будет отображать эти прогоны, пока мы не вставим их в составной node
 // это само по себе является частью дерева узлов документа, как мы сделали при первом запуске.
 // Мы можем определить, где находится текстовое содержимое узлов, которые мы вставляем
 // появляется в документе путем указания места вставки относительно другого узла в абзаце.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

 // Вставляем второй прогон в абзац перед начальным прогоном.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

 // Вставляем третий прогон после первого прогона.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

 // Вставляем первый прогон в начало коллекции дочерних узлов абзаца.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Мы можем изменить содержимое прогона, отредактировав и удалив существующие дочерние узлы.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

Показывает, как создать документ Aspose.Words вручную.

```csharp
Document doc = new Document();

 // Пустой документ по умолчанию имеет один абзац.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

 // Составные узлы, такие как наш абзац, могут содержать другие составные и встроенные узлы в качестве дочерних элементов.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

 // Создаем еще три узла запуска.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

 // Тело документа не будет отображать эти прогоны, пока мы не вставим их в составной node
 // это само по себе является частью дерева узлов документа, как мы сделали при первом запуске.
 // Мы можем определить, где находится текстовое содержимое узлов, которые мы вставляем
 // появляется в документе путем указания места вставки относительно другого узла в абзаце.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

 // Вставляем второй прогон в абзац перед начальным прогоном.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

 // Вставляем третий прогон после первого прогона.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

 // Вставляем первый прогон в начало коллекции дочерних узлов абзаца.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Мы можем изменить содержимое прогона, отредактировав и удалив существующие дочерние узлы.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

Показывает, как добавлять, обновлять и удалять дочерние узлы в коллекции дочерних узлов CompositeNode.

```csharp
Document doc = new Document();

 // Пустой документ по умолчанию имеет один абзац.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

 // Составные узлы, такие как наш абзац, могут содержать другие составные и встроенные узлы в качестве дочерних элементов.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

 // Создаем еще три узла запуска.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

 // Тело документа не будет отображать эти прогоны, пока мы не вставим их в составной node
 // это само по себе является частью дерева узлов документа, как мы сделали при первом запуске.
 // Мы можем определить, где находится текстовое содержимое узлов, которые мы вставляем
 // появляется в документе путем указания места вставки относительно другого узла в абзаце.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

 // Вставляем второй прогон в абзац перед начальным прогоном.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

 // Вставляем третий прогон после первого прогона.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

 // Вставляем первый прогон в начало коллекции дочерних узлов абзаца.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Мы можем изменить содержимое прогона, отредактировав и удалив существующие дочерние узлы.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Смотрите также

* class [Inline](../inline)
* пространство имен [Aspose.Words](../../aspose.words)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
