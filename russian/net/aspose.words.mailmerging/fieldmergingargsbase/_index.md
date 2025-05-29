---
title: FieldMergingArgsBase Class
linktitle: FieldMergingArgsBase
articleTitle: FieldMergingArgsBase
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.MailMerging.FieldMergingArgsBase — основу для эффективного слияния полей и обработки изображений при автоматизации документов.
type: docs
weight: 4470
url: /ru/net/aspose.words.mailmerging/fieldmergingargsbase/
---
## FieldMergingArgsBase class

Базовый класс для[`FieldMergingArgs`](../fieldmergingargs/) и[`ImageFieldMergingArgs`](../imagefieldmergingargs/) .

Чтобы узнать больше, посетите[Слияние писем и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) документальная статья.

```csharp
public abstract class FieldMergingArgsBase
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Возвращает[`Document`](./document/)объект, для которого выполняется слияние почты. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Получает имя поля слияния, как указано в документе. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Получает объект, представляющий текущее поле слияния. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Получает имя поля слияния в источнике данных. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Получает или задает значение поля из источника данных. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Получает индекс записи, которая объединяется, начиная с нуля. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно. |

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

* пространство имен [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../)
