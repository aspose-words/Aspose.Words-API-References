---
title: IFieldUpdatingProgressCallback Interface
linktitle: IFieldUpdatingProgressCallback
articleTitle: IFieldUpdatingProgressCallback
second_title: Aspose.Words لـ .NET
description: تتبع تقدم تحديث الحقول بسلاسة باستخدام واجهة Aspose.Words.Fields.IFieldUpdatingProgressCallback. حسّن إدارة مستنداتك اليوم!
type: docs
weight: 3140
url: /ar/net/aspose.words.fields/ifieldupdatingprogresscallback/
---
## IFieldUpdatingProgressCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد تتبع تقدم تحديث الحقل.

```csharp
public interface IFieldUpdatingProgressCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Notify](../../aspose.words.fields/ifieldupdatingprogresscallback/notify/)(*[FieldUpdatingProgressArgs](../fieldupdatingprogressargs/)*) | طريقة محددة من قبل المستخدم يتم استدعاؤها عند تغيير تقدم التحديث. |

## أمثلة

يوضح كيفية استخدام طرق الاتصال الرجعي أثناء تحديث الحقل.

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
/// قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء طرقك المخصصة أثناء تحديث الحقل.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// طريقة محددة من قبل المستخدم يتم استدعاؤها قبل تحديث الحقل مباشرةً.
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
    /// طريقة محددة من قبل المستخدم يتم استدعاؤها بعد تحديث الحقل مباشرةً.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
