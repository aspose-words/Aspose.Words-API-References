---
title: TxtLoadOptions.LeadingSpacesOptions
linktitle: LeadingSpacesOptions
articleTitle: LeadingSpacesOptions
second_title: Aspose.Words для .NET
description: TxtLoadOptions LeadingSpacesOptions свойство. Получает или задает предпочтительный параметр обработки начального пробела. Значение по умолчаниюConvertToIndent  на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.loading/txtloadoptions/leadingspacesoptions/
---
## TxtLoadOptions.LeadingSpacesOptions property

Получает или задает предпочтительный параметр обработки начального пробела. Значение по умолчанию:ConvertToIndent .

```csharp
public TxtLeadingSpacesOptions LeadingSpacesOptions { get; set; }
```

## Примеры

Показывает, как обрезать пробелы при загрузке документов с открытым текстом.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// Создаем объект «TxtLoadOptions», который мы можем передать конструктору документа
// чтобы изменить способ загрузки открытого текстового документа.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Установите для свойства "LeadingSpacesOptions" значение "TxtLeadingSpacesOptions.Preserve"
// чтобы сохранить все пробелы в начале каждой строки.
// Установите для свойства "LeadingSpacesOptions" значение "TxtLeadingSpacesOptions.ConvertToIndent"
// чтобы удалить все пробелы в начале каждой строки,
// а затем примените к абзацу отступ первой строки слева, чтобы имитировать эффект пробелов.
// Установите для свойства "LeadingSpacesOptions" значение "TxtLeadingSpacesOptions.Trim"
// чтобы удалить все пробелы в начале каждой строки.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// Установите для свойства «TrailingSpacesOptions» значение «TxtTrailingSpacesOptions.Preserve»
 // чтобы сохранить все пробелы в конце каждой строки.
 // Установите для свойства «TrailingSpacesOptions» значение «TxtTrailingSpacesOptions.Trim», чтобы
// удаляем все пробелы в конце каждой строки.
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

* enum [TxtLeadingSpacesOptions](../../txtleadingspacesoptions/)
* class [TxtLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
