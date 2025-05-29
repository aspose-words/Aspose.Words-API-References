---
title: IFieldUpdatingCallback.FieldUpdating
linktitle: FieldUpdating
articleTitle: FieldUpdating
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة IFieldUpdatingCallback—الحل الخاص بك لتحديثات الحقول المخصصة، مما يضمن الدقة والتحكم في إدارة البيانات.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/ifieldupdatingcallback/fieldupdating/
---
## IFieldUpdatingCallback.FieldUpdating method

طريقة محددة من قبل المستخدم يتم استدعاؤها قبل تحديث الحقل مباشرةً.

```csharp
public void FieldUpdating(Field field)
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

* class [Field](../../field/)
* interface [IFieldUpdatingCallback](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
