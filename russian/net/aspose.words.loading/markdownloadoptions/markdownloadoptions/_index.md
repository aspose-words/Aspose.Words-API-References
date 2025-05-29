---
title: MarkdownLoadOptions
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор MarkdownLoadOptions, позволяющий легко инициализировать экземпляры MarkdownLoadOptions для улучшенной обработки и настройки документов.
type: docs
weight: 10
url: /ru/net/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions constructor

Инициализирует новый экземпляр[`MarkdownLoadOptions`](../) класс.

```csharp
public MarkdownLoadOptions()
```

## Примечания

Автоматически устанавливает[`LoadFormat`](../../../aspose.words/loadformat/) кMarkdown .

## Примеры

Показывает, как сохранить пустую строку при загрузке документа.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Смотрите также

* class [MarkdownLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
