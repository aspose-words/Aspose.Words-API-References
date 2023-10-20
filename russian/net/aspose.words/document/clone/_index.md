---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words для .NET
description: Document Clone метод. Выполняет глубокое копированиеDocument  на С#.
type: docs
weight: 550
url: /ru/net/aspose.words/document/clone/
---
## Document.Clone method

Выполняет глубокое копирование[`Document`](../) .

```csharp
public Document Clone()
```

### Возвращаемое значение

Клонированный документ.

## Примеры

Показывает, как глубоко клонировать документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// Клонирование создаст новый документ с тем же содержимым, что и оригинал,
// но с уникальной копией каждого узла исходного документа.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
