---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words для .NET
description: Aspose.Words.HtmlInsertOptions перечисление. Определяет параметры дляInsertHtml метод на С#.
type: docs
weight: 3140
url: /ru/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Определяет параметры для[`InsertHtml`](../documentbuilder/inserthtml/) метод.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Используйте параметры по умолчанию при вставке HTML. |
| UseBuilderFormatting | `1` | Использовать шрифт и форматирование абзацев, указанное в[`DocumentBuilder`](../documentbuilder/) в качестве базового форматирования для text , вставленного из HTML. |
| RemoveLastEmptyParagraph | `2` | Удалить пустой абзац, который обычно вставляется после HTML-кода, заканчивающегося элементом уровня блока. |
| PreserveBlocks | `4` | Сохранять свойства элементов уровня блока. |

## Примеры

Показывает, как лучше сохранить видимые границы и поля.

```csharp
const string html = @"
    <html>
        <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
        </div>
    </html>";

// Устанавливаем новый режим импорта блочных элементов HTML.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
