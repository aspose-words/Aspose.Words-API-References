---
title: FieldUpdatingProgressArgs.UpdatedFieldsCount
linktitle: UpdatedFieldsCount
articleTitle: UpdatedFieldsCount
second_title: Aspose.Words для .NET
description: Откройте для себя свойство UpdatedFieldsCount объекта FieldUpdatingProgressArgs, чтобы легко отслеживать количество обновленных полей в вашем приложении.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldupdatingprogressargs/updatedfieldscount/
---
## FieldUpdatingProgressArgs.UpdatedFieldsCount property

Получает количество обновленных полей.

```csharp
public int UpdatedFieldsCount { get; }
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

* class [FieldUpdatingProgressArgs](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
