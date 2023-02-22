---
title: Interface IFieldUpdatingCallback
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.IFieldUpdatingCallback واجهه المستخدم. قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء الأساليب المخصصة الخاصة بك أثناء تحديث الحقل.
type: docs
weight: 2550
url: /ar/net/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء الأساليب المخصصة الخاصة بك أثناء تحديث الحقل.

```csharp
public interface IFieldUpdatingCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [FieldUpdated](../../aspose.words.fields/ifieldupdatingcallback/fieldupdated/)(Field) | طريقة معرّفة من قبل المستخدم يتم استدعاؤها بعد تحديث أحد الحقول مباشرةً. |
| [FieldUpdating](../../aspose.words.fields/ifieldupdatingcallback/fieldupdating/)(Field) | طريقة معرّفة من قبل المستخدم يتم استدعاؤها قبل تحديث أحد الحقول مباشرةً. |

### أمثلة

يوضح كيفية استخدام طرق رد الاتصال أثناء التحديث الميداني.

```csharp
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
public class FieldUpdatingCallback : IFieldUpdatingCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// طريقة معرّفة من قبل المستخدم يتم استدعاؤها قبل تحديث الحقل مباشرةً.
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
    /// طريقة معرّفة من قبل المستخدم يتم استدعاؤها بعد تحديث الحقل مباشرةً.
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdated(Field field)
    {
        FieldUpdatedCalls.Add(field.Result);
    }

    public IList<string> FieldUpdatedCalls { get; }
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


