---
title: Paragraph.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsMoveToRevision в Microsoft Word! Узнайте, как оно отслеживает изменения и улучшает процесс редактирования документов.
type: docs
weight: 140
url: /ru/net/aspose.words/paragraph/ismovetorevision/
---
## Paragraph.IsMoveToRevision property

Возврат`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений.

```csharp
public bool IsMoveToRevision { get; }
```

## Примеры

Показывает, как проверить, является ли абзац измененным вариантом.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Этот документ содержит редакции «Перемещение», которые появляются, когда мы выделяем текст курсором,
// а затем перетащите его, чтобы переместить в другое место
// при отслеживании изменений в Microsoft Word через «Рецензирование» -> «Отслеживать изменения».
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Перемещения ревизий состоят из пар ревизий «Переместить из» и «Переместить в».
// Эти правки представляют собой потенциальные изменения документа, которые мы можем либо принять, либо отклонить.
// Прежде чем принять/отклонить изменение хода, документ
// необходимо отслеживать как пункты отправления, так и пункты прибытия текста.
// Второй и четвертый абзацы определяют одну такую редакцию, и, таким образом, оба имеют одинаковое содержание.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// Редакция «Переместить из» — это абзац, из которого мы перетащили текст.
// Если мы примем изменения, этот абзац исчезнет,
// а другой останется и больше не будет ревизией.
Assert.True(paragraphs[1].IsMoveFromRevision);

// Редакция «Переместить в» — это абзац, в который мы перетащили текст.
// Если мы отклоним изменение, этот абзац исчезнет, а другой останется.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Смотрите также

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
