---
title: Story.Paragraphs
second_title: Справочник по API Aspose.Words для .NET
description: Story свойство. Получает коллекцию абзацев которые являются непосредственными дочерними элементами истории.
type: docs
weight: 30
url: /ru/net/aspose.words/story/paragraphs/
---
## Story.Paragraphs property

Получает коллекцию абзацев, которые являются непосредственными дочерними элементами истории.

```csharp
public ParagraphCollection Paragraphs { get; }
```

### Примеры

Показывает, как проверить, является ли абзац измененной версией.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Этот документ содержит редакции «Переместить», которые появляются, когда мы выделяем текст курсором,
// а затем перетащите его, чтобы переместить в другое место
// при отслеживании изменений в Microsoft Word через «Просмотр» -> gt; "Отслеживать изменения".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Перемещение ревизий состоит из пар ревизий «Переместить из» и «Переместить в».
// Эти поправки представляют собой потенциальные изменения в документе, которые мы можем принять или отклонить.
// Прежде чем мы примем/отклоним редакцию перемещения, документ
// должен отслеживать пункты отправления и прибытия текста.
// Второй и четвертый абзацы определяют одну такую ревизию и, следовательно, оба имеют одинаковое содержание.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// Редакция «Переместить из» — это абзац, из которого мы перетащили текст.
// Если мы примем редакцию, этот абзац исчезнет,
// а другой останется и больше не будет ревизией.
Assert.True(paragraphs[1].IsMoveFromRevision);

// Редакция «Переместить в» — это абзац, в который мы перетащили текст.
// Если мы отклоним ревизию, этот абзац исчезнет, а другой останется.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Смотрите также

* class [ParagraphCollection](../../paragraphcollection/)
* class [Story](../)
* пространство имен [Aspose.Words](../../story/)
* сборка [Aspose.Words](../../../)


