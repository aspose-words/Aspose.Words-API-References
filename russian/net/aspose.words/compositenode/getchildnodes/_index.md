---
title: GetChildNodes
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает динамическую коллекцию дочерних узлов соответствующих указанному типу.
type: docs
weight: 100
url: /ru/net/aspose.words/compositenode/getchildnodes/
---
## CompositeNode.GetChildNodes method

Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | NodeType | Задает тип узлов для выбора. |
| isDeep | Boolean | True для рекурсивного выбора из всех дочерних узлов. False для выбора только среди непосредственных дочерних элементов. |

### Возвращаемое значение

Живая коллекция дочерних узлов указанного типа.

### Примечания

Набор узлов, возвращаемый этим методом, всегда активен.

Живая коллекция всегда синхронизирована с документом. Например, если вы выбрали все разделы в документе и перебираете коллекцию удаляя разделы, раздел удаляется из коллекции немедленно когда он удаляется из документа.

### Примеры

Показывает, как распечатать все комментарии к документу и ответы на них.

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

Показывает, как извлекать изображения из документа и сохранять их в локальной файловой системе в виде отдельных файлов.

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

* class [NodeCollection](../../nodecollection)
* enum [NodeType](../../nodetype)
* class [CompositeNode](../../compositenode)
* пространство имен [Aspose.Words](../../compositenode)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
