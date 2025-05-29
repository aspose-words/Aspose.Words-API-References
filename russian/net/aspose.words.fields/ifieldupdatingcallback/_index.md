---
title: IFieldUpdatingCallback Interface
linktitle: IFieldUpdatingCallback
articleTitle: IFieldUpdatingCallback
second_title: Aspose.Words для .NET
description: Настройте обновления полей в Aspose.Words с помощью интерфейса IFieldUpdatingCallback. Расширьте функциональность с помощью собственных методов для индивидуальной обработки документов.
type: docs
weight: 3130
url: /ru/net/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface

Реализуйте этот интерфейс, если вы хотите, чтобы ваши собственные методы вызывались во время обновления поля.

```csharp
public interface IFieldUpdatingCallback
```

## Методы

| Имя | Описание |
| --- | --- |
| [FieldUpdated](../../aspose.words.fields/ifieldupdatingcallback/fieldupdated/)(*[Field](../field/)*) | Пользовательский метод, который вызывается сразу после обновления поля. |
| [FieldUpdating](../../aspose.words.fields/ifieldupdatingcallback/fieldupdating/)(*[Field](../field/)*) | Пользовательский метод, который вызывается непосредственно перед обновлением поля. |

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

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
