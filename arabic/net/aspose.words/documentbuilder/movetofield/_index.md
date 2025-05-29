---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: Aspose.Words لـ .NET
description: قم بالتنقل بسهولة عبر مستنداتك باستخدام طريقة MoveToField في DocumentBuilder، مما يسمح بتحريك المؤشر بسرعة إلى أي حقل لتحسين كفاءة التحرير.
type: docs
weight: 570
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
| isAfter | Boolean | متى`حقيقي` ، يحرك المؤشر ليكون بعد نهاية الحقل. عندما`خطأ شنيع`، يحرك المؤشر ليكون قبل بداية الحقل. |

## أمثلة

يوضح كيفية نقل مؤشر نقطة إدراج عقدة منشئ المستندات إلى حقل معين.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج حقل باستخدام DocumentBuilder وأضف سلسلة من النص بعده.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// مؤشر المنشئ موجود حاليًا في نهاية المستند.
Assert.Null(builder.CurrentNode);

// نقل المؤشر إلى الحقل مع تحديد ما إذا كان سيتم وضع هذا المؤشر قبل الحقل أو بعده.
builder.MoveToField(field, moveCursorToAfterTheField);

// لاحظ أن المؤشر يقع خارج الحقل في كلتا الحالتين.
// وهذا يعني أننا لا نستطيع تحرير الحقل باستخدام المنشئ مثل هذا.
// لتحرير حقل، يمكننا استخدام طريقة MoveTo الخاصة بالمنشئ في FieldStart الخاص بالحقل
// أو عقدة FieldSeparator لوضع المؤشر بداخلها.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
