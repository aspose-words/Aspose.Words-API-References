---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.RevisionsView, чтобы легко выбирать между исходными и измененными версиями документа для упрощения редактирования и совместной работы.
type: docs
weight: 5550
url: /ru/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

Позволяет указать, следует ли работать с исходной или измененной версией документа.

```csharp
public enum RevisionsView
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Original | `0` | Указывает исходную версию документа. |
| Final | `1` | Указывает пересмотренную версию документа. |

## Примеры

Показывает, как переключаться между измененным и исходным видом документа.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Просмотр объекта документа, как будто все изменения приняты. В настоящее время поддерживает списочные метки.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
