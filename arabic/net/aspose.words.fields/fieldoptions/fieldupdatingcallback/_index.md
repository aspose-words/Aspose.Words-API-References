---
title: FieldOptions.FieldUpdatingCallback
linktitle: FieldUpdatingCallback
articleTitle: FieldUpdatingCallback
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldOptions FieldUpdatingCallback لإدارة تنفيذات IFieldUpdatingCallback بسهولة وتعزيز كفاءة التعامل مع البيانات.
type: docs
weight: 120
url: /ar/net/aspose.words.fields/fieldoptions/fieldupdatingcallback/
---
## FieldOptions.FieldUpdatingCallback property

يحصل أو يعين[`IFieldUpdatingCallback`](../../ifieldupdatingcallback/) التنفيذ

```csharp
public IFieldUpdatingCallback FieldUpdatingCallback { get; set; }
```

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

* interface [IFieldUpdatingCallback](../../ifieldupdatingcallback/)
* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
