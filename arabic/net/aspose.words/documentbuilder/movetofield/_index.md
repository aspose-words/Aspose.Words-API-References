---
title: DocumentBuilder.MoveToField
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. يحرك المؤشر إلى حقل في المستند.
type: docs
weight: 540
url: /ar/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

يحرك المؤشر إلى حقل في المستند.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| field | Field | الحقل الذي سيتم نقل المؤشر إليه. |
| isAfter | Boolean | متى`حقيقي` ، يحرك المؤشر ليكون بعد نهاية الحقل. متى`خطأ شنيع`، يحرك المؤشر ليكون قبل بدء الحقل. |

### أمثلة

يوضح كيفية نقل مؤشر نقطة إدراج عقدة منشئ المستندات إلى حقل معين.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقلاً باستخدام DocumentBuilder وأضف سلسلة من النص بعده.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// مؤشر المنشئ موجود حاليًا في نهاية المستند.
Assert.Null(builder.CurrentNode);

// حرك المؤشر إلى الحقل أثناء تحديد ما إذا كنت تريد وضع هذا المؤشر قبل الحقل أم بعده.
builder.MoveToField(field, moveCursorToAfterTheField);

// لاحظ أن المؤشر خارج الحقل في كلتا الحالتين.
// هذا يعني أنه لا يمكننا تعديل الحقل باستخدام المنشئ بهذه الطريقة.
// لتحرير حقل، يمكننا استخدام طريقة MoveTo الخاصة بالمنشئ في FieldStart الخاص بالحقل
// أو عقدة FieldSeparator لوضع المؤشر بالداخل.
if (moveCursorToAfterTheField)
{
    Assert.Null(builder.CurrentNode);
    builder.Write(" Text immediately after the field.");

    Assert.AreEqual("\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", 
        doc.GetText().Trim());
}
else
{
    Assert.AreEqual(field.Start, builder.CurrentNode);
    builder.Write("Text immediately before the field. ");

    Assert.AreEqual("Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", 
        doc.GetText().Trim());
}
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


