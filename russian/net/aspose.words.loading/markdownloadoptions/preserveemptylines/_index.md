---
title: MarkdownLoadOptions.PreserveEmptyLines
linktitle: PreserveEmptyLines
articleTitle: PreserveEmptyLines
second_title: Aspose.Words для .NET
description: Узнайте, как свойство MarkdownLoadOptions PreserveEmptyLines улучшает загрузку документов Markdown, сохраняя пустые строки для улучшения читабельности.
type: docs
weight: 30
url: /ru/net/aspose.words.loading/markdownloadoptions/preserveemptylines/
---
## MarkdownLoadOptions.PreserveEmptyLines property

Возвращает или задает логическое значение, указывающее, следует ли сохранять пустые строки при загрузкеMarkdown document. Значение по умолчанию:`ЛОЖЬ` .

Обычно пустые строки между элементами уровня блока в Markdown игнорируются. Пустые строки в начале и конце документа также игнорируются. Эта опция позволяет импортировать такие пустые строки.

```csharp
public bool PreserveEmptyLines { get; set; }
```

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
