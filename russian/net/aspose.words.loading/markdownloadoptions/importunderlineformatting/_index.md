---
title: MarkdownLoadOptions.ImportUnderlineFormatting
linktitle: ImportUnderlineFormatting
articleTitle: ImportUnderlineFormatting
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MarkdownLoadOptions ImportUnderlineFormatting. Управляйте форматированием подчеркивания текста с помощью простой логической настройки. Улучшите свой опыт работы с Markdown!
type: docs
weight: 20
url: /ru/net/aspose.words.loading/markdownloadoptions/importunderlineformatting/
---
## MarkdownLoadOptions.ImportUnderlineFormatting property

Возвращает или задает логическое значение, указывающее, следует ли распознавать последовательность из двух символов плюс "++" как подчеркивание форматирования текста. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ImportUnderlineFormatting { get; set; }
```

## Примеры

Показывает, как распознавать символы «++» как подчеркивание форматирования текста.

```csharp
using (MemoryStream stream = new MemoryStream(Encoding.ASCII.GetBytes("++12 and B++")))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = true };
    Document doc = new Document(stream, loadOptions);

    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.Single, para.Runs[0].Font.Underline);

    loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = false };
    doc = new Document(stream, loadOptions);

    para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.None, para.Runs[0].Font.Underline);
}
```

### Смотрите также

* class [MarkdownLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
