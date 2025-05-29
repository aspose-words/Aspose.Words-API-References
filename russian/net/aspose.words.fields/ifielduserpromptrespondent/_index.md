---
title: IFieldUserPromptRespondent Interface
linktitle: IFieldUserPromptRespondent
articleTitle: IFieldUserPromptRespondent
second_title: Aspose.Words для .NET
description: Откройте для себя интерфейс Aspose.Words.Fields.IFieldUserPromptRespondent, разработанный для улучшения взаимодействия с пользователем и упрощения обновления полей.
type: docs
weight: 3150
url: /ru/net/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface

Представляет респондента на запросы пользователя во время обновления поля.

```csharp
public interface IFieldUserPromptRespondent
```

## Методы

| Имя | Описание |
| --- | --- |
| [Respond](../../aspose.words.fields/ifielduserpromptrespondent/respond/)(*string, string*) | При реализации возвращает ответ пользователя на запрос. Ваша реализация должна возвращать`нулевой` чтобы указать, что пользователь не ответил на приглашение (т.е. пользователь нажал кнопку «Отмена» в окне приглашения). |

## Примечания

Поля ASK и FILLIN являются примерами полей, которые запрашивают у пользователя какой-либо ответ. Реализуйте этот интерфейс и назначьте его[`UserPromptRespondent`](../fieldoptions/userpromptrespondent/) свойство для установления взаимодействия между полем update и пользователем.

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

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
