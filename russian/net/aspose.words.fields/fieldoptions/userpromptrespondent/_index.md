---
title: FieldOptions.UserPromptRespondent
linktitle: UserPromptRespondent
articleTitle: UserPromptRespondent
second_title: Aspose.Words для .NET
description: Узнайте, как свойство FieldOptions UserPromptRespondent улучшает пользовательский опыт, управляя взаимодействием с респондентами во время обновления полей.
type: docs
weight: 220
url: /ru/net/aspose.words.fields/fieldoptions/userpromptrespondent/
---
## FieldOptions.UserPromptRespondent property

Получает или задает респонденту подсказки пользователя во время обновления поля.

```csharp
public IFieldUserPromptRespondent UserPromptRespondent { get; set; }
```

## Примечания

Если значение этого свойства установлено равным`нулевой` , поля, требующие ответа пользователя на prompting (например,[`FieldAsk`](../../fieldask/) или[`FieldFillIn`](../../fieldfillin/)) не обновляются.

Значение по умолчанию:`нулевой`.

## Примеры

Показывает, как создать поле ASK и задать его свойства.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Размещаем поле, в которое будет помещен ответ на наше поле ASK.
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

    // Мы можем изменить или переопределить ответ по умолчанию в наших полях ASK с помощью пользовательского ответчика на подсказки,
    // что произойдет во время слияния почты.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Добавляет текст к ответу по умолчанию поля ASK во время слияния почты.
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
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
