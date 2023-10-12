---
title: DocumentBuilder.InsertHtml
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Вставляет в документ HTMLстроку.
type: docs
weight: 360
url: /ru/net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(string) {#inserthtml}

Вставляет в документ HTML-строку.

```csharp
public void InsertHtml(string html)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| html | String | Строка HTML для вставки в документ. |

### Примечания

Вы можете использовать этот метод для вставки фрагмента HTML или всего документа HTML.

### Примеры

Показывает, как использовать построитель документов для вставки HTML-содержимого в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" + 
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" + 
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// Вставка HTML-кода анализирует форматирование каждого элемента в эквивалентное форматирование текста документа.
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual("Paragraph right", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

Assert.AreEqual("Implicit paragraph left", paragraphs[1].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.True(paragraphs[1].Runs[0].Font.Bold);

Assert.AreEqual("Div center", paragraphs[2].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Center, paragraphs[2].ParagraphFormat.Alignment);

Assert.AreEqual("Heading 1 left.", paragraphs[3].GetText().Trim());
Assert.AreEqual("Heading 1", paragraphs[3].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtml.docx");
```

Показывает, как выполнить слияние почты с помощью пользовательского обратного вызова, который обрабатывает данные слияния в форме документов HTML.

```csharp
public void MergeHtml()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// Если при слиянии почты встречается MERGEFIELD, имя которого начинается с префикса "html_",
/// этот обратный вызов анализирует свои данные слияния как содержимое HTML и добавляет результат в местоположение документа MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Вызывается, когда слияние почты объединяет данные в MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Добавляем проанализированные данные HTML в тело документа.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Поскольку мы уже вставили объединенный контент вручную,
             // нам не нужно будет реагировать на это событие, возвращая контент через свойство «Текст».
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Ничего не делать.
    }
}
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)

---

## InsertHtml(string, bool) {#inserthtml_2}

Вставляет в документ HTML-строку.

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| html | String | Строка HTML для вставки в документ. |
| useBuilderFormatting | Boolean | Значение, указывающее, указано ли форматирование, указанное в[`DocumentBuilder`](../) используется в качестве базового форматирования текста, импортированного из HTML. |

### Примечания

Вы можете использовать этот метод для вставки фрагмента HTML или всего документа HTML.

Когда*useBuilderFormatting* является`ЛОЖЬ` , [`DocumentBuilder`](../)форматирование игнорируется, а форматирование вставленного text основано на форматировании HTML по умолчанию. В результате текст выглядит так, как он отображается в браузерах.

Когда*useBuilderFormatting* является`истинный` , форматирование вставленного текста основано на[`DocumentBuilder`](../) форматирование, и текст выглядит так, как будто он был вставлен с помощью[`Write`](../write/) .

### Примеры

Показывает, как применить форматирование построителя документов при вставке содержимого HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите выравнивание текста для компоновщика, вставьте абзац HTML с указанным выравниванием и без него.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// Для первого абзаца указано выравнивание. Когда InsertHtml анализирует HTML-код,
// значение выравнивания абзаца, найденное в HTML-коде, всегда заменяет значение построителя документа.
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

// Для второго абзаца не указано выравнивание. Он может иметь значение выравнивания, заполненное
// по значению строителя в зависимости от флага, который мы передали методу InsertHtml.
Assert.AreEqual("Paragraph 2.", paragraphs[1].GetText().Trim());
Assert.AreEqual(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left,
    paragraphs[1].ParagraphFormat.Alignment);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)

---

## InsertHtml(string, HtmlInsertOptions) {#inserthtml_1}

Вставляет в документ строку HTML. Позволяет указать дополнительные параметры.

```csharp
public void InsertHtml(string html, HtmlInsertOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| html | String | Строка HTML для вставки в документ. |
| options | HtmlInsertOptions | Параметры, которые используются при вставке строки HTML. |

### Примечания

Вы можете использовать этот метод для вставки фрагмента HTML или всего документа HTML.

### Примеры

Показывает, как использовать параметры при вставке HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// По умолчанию «DocumentBuilder.InsertHtml» вставляет фрагмент HTML, который заканчивается элементом HTML уровня блока,
// обычно он закрывает этот элемент уровня блока и вставляет разрыв абзаца.
// В результате после вставленного документа появляется новый пустой абзац.
// Если мы укажем «HtmlInsertOptions.RemoveLastEmptyParagraph», эти лишние пустые абзацы будут удалены.
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### Смотрите также

* enum [HtmlInsertOptions](../../htmlinsertoptions/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


