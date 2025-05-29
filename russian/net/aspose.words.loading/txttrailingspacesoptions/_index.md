---
title: TxtTrailingSpacesOptions Enum
linktitle: TxtTrailingSpacesOptions
articleTitle: TxtTrailingSpacesOptions
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.TxtTrailingSpacesOptions для эффективного управления конечным пробелом при импорте текстовых файлов. Улучшите обработку документов сегодня!
type: docs
weight: 4200
url: /ru/net/aspose.words.loading/txttrailingspacesoptions/
---
## TxtTrailingSpacesOptions enumeration

Указывает доступные параметры обработки конечных пробелов во время импорта изText файл.

```csharp
public enum TxtTrailingSpacesOptions
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Trim | `0` | Конечные пробелы обрезаются. |
| Preserve | `1` | Конечные пробелы сохраняются. |

## Примеры

Показывает, как обрезать пробелы при загрузке текстовых документов.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// Создаем объект "TxtLoadOptions", который можно передать конструктору документа
// чтобы изменить способ загрузки текстового документа.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Установите свойство "LeadingSpacesOptions" на "TxtLeadingSpacesOptions.Preserve"
// для сохранения всех пробельных символов в начале каждой строки.
// Установите свойство "LeadingSpacesOptions" на "TxtLeadingSpacesOptions.ConvertToIndent"
// чтобы удалить все пробельные символы в начале каждой строки,
// а затем применяем отступ левой первой строки к абзацу, чтобы имитировать эффект пробелов.
// Установите свойство "LeadingSpacesOptions" на "TxtLeadingSpacesOptions.Trim"
// для удаления всех пробельных символов в начале каждой строки.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// Установите свойство "TrailingSpacesOptions" на "TxtTrailingSpacesOptions.Preserve"
 // для сохранения всех пробельных символов в конце каждой строки.
 // Установите свойство "TrailingSpacesOptions" в "TxtTrailingSpacesOptions.Trim" для
// удалить все пробельные символы в конце каждой строки.
loadOptions.TrailingSpacesOptions = txtTrailingSpacesOptions;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

switch (txtLeadingSpacesOptions)
{
    case TxtLeadingSpacesOptions.ConvertToIndent:
        Assert.AreEqual(37.8d, paragraphs[0].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(25.2d, paragraphs[1].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(6.3d, paragraphs[2].ParagraphFormat.FirstLineIndent);

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
    case TxtLeadingSpacesOptions.Preserve:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("      Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("    Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith(" Line 3"));
        break;
    case TxtLeadingSpacesOptions.Trim:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
}

switch (txtTrailingSpacesOptions)
{
    case TxtTrailingSpacesOptions.Preserve:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1 \r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2   \r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3       \f"));
        break;
    case TxtTrailingSpacesOptions.Trim:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1\r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2\r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3\f"));
        break;
}
```

### Смотрите также

* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
