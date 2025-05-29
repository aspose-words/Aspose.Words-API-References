---
title: Paragraph.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words для .NET
description: Откройте для себя метод Paragraph GetText, который позволяет легко извлекать текст, включая окончания абзацев, повышая эффективность обработки текста.
type: docs
weight: 280
url: /ru/net/aspose.words/paragraph/gettext/
---
## Paragraph.GetText method

Получает текст этого абзаца, включая символ конца абзаца.

```csharp
public override string GetText()
```

## Примечания

Текст всех дочерних узлов объединяется, и добавляется символ конца абзаца следующим образом:

* Если абзац является последним абзацем[`Body`](../../body/) , тогда [`SectionBreak`](../../controlchar/sectionbreak/) (\x000c) добавляется.
* Если абзац является последним абзацем[`Cell`](../../../aspose.words.tables/cell/) , тогда [`Cell`](../../controlchar/cell/) (\x0007) добавляется.
* Для всех остальных параграфов [`ParagraphBreak`](../../controlchar/paragraphbreak/) (\r) добавляется.

Возвращаемая строка включает все управляющие и специальные символы, как описано в[`ControlChar`](../../controlchar/).

## Примеры

Показывает, как добавлять, обновлять и удалять дочерние узлы в коллекции дочерних узлов CompositeNode.

```csharp
Document doc = new Document();

// Пустой документ по умолчанию имеет один абзац.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Составные узлы, такие как наш абзац, могут содержать другие составные и встроенные узлы в качестве дочерних.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Создаем еще три узла запуска.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Тело документа не будет отображать эти прогоны, пока мы не вставим их в составной узел
// который сам по себе является частью дерева узлов документа, как мы это делали при первом запуске.
// Мы можем определить, где находится текстовое содержимое узлов, которые мы вставляем
// появляется в документе, указывая место вставки относительно другого узла в абзаце.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Вставьте вторую строку в абзац перед первой строкой.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Вставьте третий запуск после первого запуска.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Вставляем первую строку в начало коллекции дочерних узлов абзаца.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Мы можем изменить содержимое прогона, редактируя и удаляя существующие дочерние узлы.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Смотрите также

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
