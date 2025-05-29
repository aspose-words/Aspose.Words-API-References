---
title: FieldMergingArgs.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: Управляйте полями слияния вашего документа без усилий с помощью FieldMergingArgs. Легко устанавливайте или извлекайте текст для бесшовной интеграции документа.
type: docs
weight: 10
url: /ru/net/aspose.words.mailmerging/fieldmergingargs/text/
---
## FieldMergingArgs.Text property

Возвращает или задает текст, который будет вставлен в документ для текущего поля слияния.

```csharp
public string Text { get; set; }
```

## Примечания

При вызове обработчика событий это свойство устанавливается в значение`нулевой`.

Если вы оставите Текст как`нулевой` , движок слияния почты вставит[`FieldValue`](../../fieldmergingargsbase/fieldvalue/) вместо поля слияния.

Если задать для параметра Текст любую строку (включая пустую), эта строка будет вставлена в документ вместо поля слияния.

## Примеры

Показывает, как выполнить слияние почты с помощью настраиваемого обратного вызова, который обрабатывает данные слияния в форме HTML-документов.

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
/// Если при слиянии почты обнаруживается MERGEFIELD, имя которого начинается с префикса "html_",
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
            // Добавить проанализированные HTML-данные в тело документа.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Поскольку мы уже вставили объединенный контент вручную,
            // нам не нужно будет реагировать на это событие, возвращая содержимое через свойство "Текст".
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
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
