---
title: Field.IsDirty
second_title: Aspose.Words لمراجع .NET API
description: Field ملكية. الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة قديمة بسبب تعديلات أخرى تم إجراؤها على المستند.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/field/isdirty/
---
## Field.IsDirty property

الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند.

```csharp
public bool IsDirty { get; set; }
```

### أمثلة

يوضح كيفية استخدام خاصية خاصة لتحديث نتيجة الحقل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أعط قيمة خاصية "المؤلف" المضمنة في المستند، ثم اعرضها مع حقل.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// تحديث الخاصية. لا يزال الحقل يعرض القيمة القديمة.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// نظرًا لأن قيمة الحقل قديمة، فيمكننا وضع علامة عليها على أنها "متسخة".
// ستظل هذه القيمة قديمة حتى نقوم بتحديث الحقل يدويًا باستخدام طريقة Field.Update().
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // إذا قمنا بالحفظ دون استدعاء طريقة التحديث،
    // سيستمر الحقل في عرض القيمة القديمة في مستند الإخراج.
    doc.Save(docStream, SaveFormat.Docx);

    // يحتوي كائن LoadOptions على خيار لتحديث جميع الحقول
    // تم وضع علامة "قذرة" عند تحميل المستند.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // يؤدي تحديث الحقول القذرة مثل هذا إلى تعيين علامة "IsDirty" الخاصة بها تلقائيًا على "خطأ".
    if (updateDirtyFields)
    {
        Assert.AreEqual("John & Jane Doe", field.Result);
        Assert.False(field.IsDirty);
    }
    else
    {
        Assert.AreEqual("John Doe", field.Result);
        Assert.True(field.IsDirty);
    }
}
```

### أنظر أيضا

* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../field/)
* المجسم [Aspose.Words](../../../)


