---
title: Interface IFieldUpdatingCallback
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.IFieldUpdatingCallback واجهه المستخدم. قم بتنفيذ هذه الواجهة إذا كنت تريد أن يتم استدعاء الأساليب المخصصة الخاصة بك أثناء التحديث الميداني.
type: docs
weight: 2720
url: /ar/net/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد أن يتم استدعاء الأساليب المخصصة الخاصة بك أثناء التحديث الميداني.

```csharp
public interface IFieldUpdatingCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [FieldUpdated](../../aspose.words.fields/ifieldupdatingcallback/fieldupdated/)(Field) | طريقة يحددها المستخدم ويتم استدعاؤها مباشرة بعد تحديث الحقل. |
| [FieldUpdating](../../aspose.words.fields/ifieldupdatingcallback/fieldupdating/)(Field) | طريقة يحددها المستخدم ويتم استدعاؤها قبل تحديث الحقل مباشرة. |

### أمثلة

يوضح كيفية استخدام طرق رد الاتصال أثناء التحديث الميداني.

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
/// قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء الأساليب المخصصة الخاصة بك أثناء التحديث الميداني.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// طريقة يحددها المستخدم يتم استدعاؤها قبل تحديث الحقل مباشرةً.
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
    /// طريقة يحددها المستخدم يتم استدعاؤها مباشرة بعد تحديث الحقل.
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


