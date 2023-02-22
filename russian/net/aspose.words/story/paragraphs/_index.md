---
title: Story.Paragraphs
second_title: Справочник по API Aspose.Words для .NET
description: Story свойство. Получает набор абзацев которые являются непосредственными дочерними элементами статьи.
type: docs
weight: 30
url: /ru/net/aspose.words/story/paragraphs/
---
## Story.Paragraphs property

Получает набор абзацев, которые являются непосредственными дочерними элементами статьи.

```csharp
public ParagraphCollection Paragraphs { get; }
```

### Примеры

Показывает, как проверить, является ли абзац ревизией перемещения.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Этот документ содержит ревизии «Переместить», которые появляются, когда мы выделяем текст курсором,
// а затем перетащите его, чтобы переместить в другое место
// при отслеживании редакций в Microsoft Word через "Рецензирование" -> "Отслеживать изменения".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// Перемещение ревизий состоит из пар ревизий «Переместить из» и «Переместить в». 
// Эти исправления являются потенциальными изменениями в документе, которые мы можем либо принять, либо отклонить.
// Прежде чем мы примем/отклоним ревизию перемещения, документ
// должен отслеживать места отправления и прибытия текста.
// Второй и четвертый абзацы определяют одну такую ревизию, поэтому оба имеют одинаковое содержимое.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// Редакция «Переместить из» — это абзац, из которого мы перетащили текст.
// Если мы примем исправление, этот абзац исчезнет,
// а другой останется и уже не будет ревизией.
Assert.True(paragraphs[1].IsMoveFromRevision);

// Редакция «Переместить в» — это абзац, в который мы перетащили текст.
// Если мы отклоним исправление, этот абзац вместо этого исчезнет, а другой останется.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Смотрите также

* class [ParagraphCollection](../../paragraphcollection/)
* class [Story](../)
* пространство имен [Aspose.Words](../../story/)
* сборка [Aspose.Words](../../../)


