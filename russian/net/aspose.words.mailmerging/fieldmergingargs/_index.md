---
title: Class FieldMergingArgs
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.MailMerging.FieldMergingArgs сорт. Предоставляет данные для Объединить поле событие.
type: docs
weight: 3770
url: /ru/net/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class

Предоставляет данные для **Объединить поле** событие.

Чтобы узнать больше, посетите[Слияние почты и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) статья документации.

```csharp
public class FieldMergingArgs : FieldMergingArgsBase
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Возвращает[`Document`](../fieldmergingargsbase/document/) объект, для которого выполняется слияние почты. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Получает имя поля слияния, указанное в документе. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Получает объект, представляющий текущее поле слияния. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Получает имя поля слияния в источнике данных. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Получает или задает значение поля из источника данных. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Получает индекс объединяемой записи, начинающийся с нуля. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно. |
| [Text](../../aspose.words.mailmerging/fieldmergingargs/text/) { get; set; } | Получает или задает текст, который будет вставлен в документ для текущего поля слияния. |

### Примечания

**Объединить поле** Событие происходит во время слияния почты, когда в документе встречается простое поле mail merge . Вы можете ответить на это событие текстом return , который механизм слияния почты вставит в документ.

### Примеры

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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* пространство имен [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../)


