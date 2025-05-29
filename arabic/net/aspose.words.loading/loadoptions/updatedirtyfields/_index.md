---
title: LoadOptions.UpdateDirtyFields
linktitle: UpdateDirtyFields
articleTitle: UpdateDirtyFields
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية LoadOptions UpdateDirtyFields على تعزيز سلامة البيانات من خلال تحديث الحقول التي تم وضع علامة عليها على أنها متسخة بشكل انتقائي لتحقيق الأداء الأمثل.
type: docs
weight: 160
url: /ar/net/aspose.words.loading/loadoptions/updatedirtyfields/
---
## LoadOptions.UpdateDirtyFields property

يحدد ما إذا كان سيتم تحديث الحقول باستخدام`متسخ` السمة.

```csharp
public bool UpdateDirtyFields { get; set; }
```

## أمثلة

يوضح كيفية استخدام الخاصية الخاصة لتحديث نتيجة الحقل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإعطاء قيمة الخاصية "المؤلف" المضمنة في المستند، ثم قم بعرضها باستخدام الحقل.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// تحديث الخاصية. لا يزال الحقل يعرض القيمة القديمة.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// بما أن قيمة الحقل قديمة، فيمكننا وضع علامة عليها بأنها "غير صالحة".
// ستظل هذه القيمة قديمة حتى نقوم بتحديث الحقل يدويًا باستخدام طريقة Field.Update().
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // إذا قمنا بالحفظ دون استدعاء طريقة التحديث،
    // سيستمر الحقل في عرض القيمة القديمة في المستند الناتج.
    doc.Save(docStream, SaveFormat.Docx);

    // يحتوي كائن LoadOptions على خيار لتحديث جميع الحقول
    // تم وضع علامة "متسخ" عند تحميل المستند.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // يؤدي تحديث الحقول المتسخة مثل هذا إلى تعيين علامة "IsDirty" الخاصة بها إلى false تلقائيًا.
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

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
