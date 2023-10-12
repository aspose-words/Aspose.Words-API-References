---
title: FieldOptions.UserPromptRespondent
second_title: Справочник по API Aspose.Words для .NET
description: FieldOptions свойство. Получает или задает респондента на запросы пользователя во время обновления поля.
type: docs
weight: 220
url: /ru/net/aspose.words.fields/fieldoptions/userpromptrespondent/
---
## FieldOptions.UserPromptRespondent property

Получает или задает респондента на запросы пользователя во время обновления поля.

```csharp
public IFieldUserPromptRespondent UserPromptRespondent { get; set; }
```

### Примечания

Если значение этого свойства установлено равным`нулевой` , поля, которые требуют ответа пользователя на Promting (например,[`FieldAsk`](../../fieldask/) или[`FieldFillIn`](../../fieldfillin/)) не обновляются.

Значение по умолчанию:`нулевой`.

### Примеры

Показывает, как создать поле ASK и настроить его свойства.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Размещаем поле, в котором будет размещен ответ на наше поле ASK.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // Вставьте поле ASK и отредактируйте его свойства, чтобы ссылаться на наше поле REF по имени закладки.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // Поля ASK применяют ответ по умолчанию к соответствующим полям REF во время слияния почты.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // Мы можем изменить или переопределить ответ по умолчанию в наших полях ASK с помощью специального ответчика на приглашение,
    // что произойдет во время слияния почты.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Добавляет текст к ответу по умолчанию в поле ASK во время слияния почты.
/// </summary>
private class MyPromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response from MyPromptRespondent. " + defaultResponse;
    }
}
```

### Смотрите также

* interface [IFieldUserPromptRespondent](../../ifielduserpromptrespondent/)
* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../fieldoptions/)
* сборка [Aspose.Words](../../../)


