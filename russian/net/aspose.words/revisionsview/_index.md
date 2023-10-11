---
title: Enum RevisionsView
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.RevisionsView перечисление. Позволяет указать работать ли с исходной или исправленной версией документа.
type: docs
weight: 4810
url: /ru/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

Позволяет указать, работать ли с исходной или исправленной версией документа.

```csharp
public enum RevisionsView
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Original | `0` | Указывает исходную версию документа. |
| Final | `1` | Указывает исправленную версию документа. |

### Примеры

Показывает, как переключаться между измененным и исходным видом документа.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Просматриваем объект документа так, как будто все изменения приняты. В настоящее время поддерживаются метки списков.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


