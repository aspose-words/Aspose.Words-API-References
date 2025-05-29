---
title: IFieldUpdatingCallback.FieldUpdating
linktitle: FieldUpdating
articleTitle: FieldUpdating
second_title: Aspose.Words для .NET
description: Откройте для себя метод IFieldUpdatingCallback — ваше решение для обновления пользовательских полей, обеспечивающее точность и контроль при управлении данными.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/ifieldupdatingcallback/fieldupdating/
---
## IFieldUpdatingCallback.FieldUpdating method

Пользовательский метод, который вызывается непосредственно перед обновлением поля.

```csharp
public void FieldUpdating(Field field)
```

## Примеры

Показывает, как использовать методы обратного вызова во время обновления поля.

```csharp
public void FieldUpdatingCallbackTest()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");

    FieldUpdatingCallback callback = new FieldUpdatingCallback();
    doc.FieldOptions.FieldUpdatingCallback = callback;

    doc.UpdateFields();

    Assert.True(callback.FieldUpdatedCalls.Contains("Updating John Doe"));
}

/// <summary>
/// Реализуйте этот интерфейс, если вы хотите, чтобы ваши собственные методы вызывались во время обновления поля.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// Пользовательский метод, который вызывается непосредственно перед обновлением поля.
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdating(Field field)
    {
        if (field.Type == FieldType.FieldAuthor)
        {
            FieldAuthor fieldAuthor = (FieldAuthor) field;
            fieldAuthor.AuthorName = "Updating John Doe";
        }
    }

    /// <summary>
    /// Пользовательский метод, который вызывается сразу после обновления поля.
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdated(Field field)
    {
        FieldUpdatedCalls.Add(field.Result);
    }

    void IFieldUpdatingProgressCallback.Notify(FieldUpdatingProgressArgs args)
    {
        Console.WriteLine($"{args.UpdateCompleted}/{args.TotalFieldsCount}");
        Console.WriteLine($"{args.UpdatedFieldsCount}");
    }

    public IList<string> FieldUpdatedCalls { get; }
}
```

### Смотрите также

* class [Field](../../field/)
* interface [IFieldUpdatingCallback](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
