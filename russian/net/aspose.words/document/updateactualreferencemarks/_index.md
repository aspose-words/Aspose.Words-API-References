---
title: Document.UpdateActualReferenceMarks
linktitle: UpdateActualReferenceMarks
articleTitle: UpdateActualReferenceMarks
second_title: Aspose.Words для .NET
description: С легкостью обновляйте все сноски и концевые сноски в документе с помощью метода Document UpdateActualReferenceMarks, повышая точность и эффективность.
type: docs
weight: 800
url: /ru/net/aspose.words/document/updateactualreferencemarks/
---
## Document.UpdateActualReferenceMarks method

Обновляет[`ActualReferenceMark`](../../../aspose.words.notes/footnote/actualreferencemark/) свойство всех сносок и концевых сносок в документе.

```csharp
public void UpdateActualReferenceMarks()
```

## Примечания

Обновление полей ([`UpdateFields`](../updatefields/) ) может быть необходимо для получения правильного результата.

## Примеры

Показывает, как получить реальный знак ссылки на сноску.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

Footnote footnote = (Footnote)doc.GetChild(NodeType.Footnote, 1, true);
doc.UpdateFields();
doc.UpdateActualReferenceMarks();

Assert.AreEqual("1", footnote.ActualReferenceMark);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
