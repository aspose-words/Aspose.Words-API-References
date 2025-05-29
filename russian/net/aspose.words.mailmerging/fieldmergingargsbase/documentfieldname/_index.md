---
title: FieldMergingArgsBase.DocumentFieldName
linktitle: DocumentFieldName
articleTitle: DocumentFieldName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DocumentFieldName FieldMergingArgsBase. Легко получайте доступ и управляйте именами полей слияния для эффективной обработки документов.
type: docs
weight: 20
url: /ru/net/aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/
---
## FieldMergingArgsBase.DocumentFieldName property

Получает имя поля слияния, как указано в документе.

```csharp
public string DocumentFieldName { get; }
```

## Примечания

Если у вас есть сопоставление имени поля документа с другим именем поля источника данных, , то это исходное имя поля, указанное в документе.

Если вы указали префикс имени поля, например, «Image:MyFieldName» в документе, , то`DocumentFieldName` возвращает имя поля без префикса, то есть «MyFieldName».

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

* class [FieldMergingArgsBase](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
