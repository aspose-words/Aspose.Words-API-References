---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words для .NET
description: Document OriginalLoadFormat свойство. Получает формат исходного документа который был загружен в этот объект на С#.
type: docs
weight: 300
url: /ru/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Получает формат исходного документа, который был загружен в этот объект.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## Примечания

Если вы создали новый пустой документ, возвращаетDoc ценить.

## Примеры

Показывает, как получить сведения об операции загрузки документа.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### Смотрите также

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
