---
title: FieldUpdating
second_title: Aspose.Words لمراجع .NET API
description: طريقة معرّفة من قبل المستخدم يتم استدعاؤها قبل تحديث أحد الحقول مباشرةً.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/ifieldupdatingcallback/fieldupdating/
---
## IFieldUpdatingCallback.FieldUpdating method

طريقة معرّفة من قبل المستخدم يتم استدعاؤها قبل تحديث أحد الحقول مباشرةً.

```csharp
public void FieldUpdating(Field field)
```

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

* class [Field](../../field)
* interface [IFieldUpdatingCallback](../../ifieldupdatingcallback)
* مساحة الاسم [Aspose.Words.Fields](../../ifieldupdatingcallback)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->