---
title: FieldMergingArgs.Text
second_title: Справочник по API Aspose.Words для .NET
description: FieldMergingArgs свойство. Получает или задает текст который будет вставлен в документ для текущего поля слияния.
type: docs
weight: 10
url: /ru/net/aspose.words.mailmerging/fieldmergingargs/text/
---
## FieldMergingArgs.Text property

Получает или задает текст, который будет вставлен в документ для текущего поля слияния.

```csharp
public string Text { get; set; }
```

### Примечания

При вызове обработчика событий этому свойству присваивается значение null.

Если вы оставите Text равным нулю, механизм слияния писем вставит[`FieldValue`](../../fieldmergingargsbase/fieldvalue/) вместо поля слияния.

Если вы установите Text на любую строку (включая пустую), строка будет вставлена в документ вместо поля слияния.

### Примеры

Показывает, как выполнить слияние почты с помощью пользовательского обратного вызова, который обрабатывает данные слияния в виде HTML-документов.

```csharp
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
/// Если слияние почты встречает MERGEFIELD, имя которого начинается с префикса "html_",
/// этот обратный вызов анализирует свои данные слияния как содержимое HTML и добавляет результат в расположение документа MERGEFIELD.
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
            // Добавляем проанализированные HTML-данные в тело документа.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Так как мы уже вставили объединенный контент вручную,
             // нам не нужно будет реагировать на это событие, возвращая содержимое через свойство «Текст».
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

* class [FieldMergingArgs](../)
* пространство имен [Aspose.Words.MailMerging](../../fieldmergingargs/)
* сборка [Aspose.Words](../../../)


