---
title: TextFormFieldType Enum
linktitle: TextFormFieldType
articleTitle: TextFormFieldType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.TextFormFieldType تعداد. يحدد نوع حقل النموذج النصي في C#.
type: docs
weight: 2770
url: /ar/net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

يحدد نوع حقل النموذج النصي.

```csharp
public enum TextFormFieldType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Regular | `0` | يمكن أن يحتوي حقل النموذج النصي على أي نص. |
| Number | `1` | يمكن أن يحتوي حقل النموذج النصي على أرقام فقط. |
| Date | `2` | يمكن أن يحتوي حقل النموذج النصي على قيمة تاريخ صالحة فقط. |
| CurrentDate | `3` | قيمة حقل النموذج النصي هي التاريخ الحالي عند تحديث الحقل. |
| CurrentTime | `4` | قيمة حقل النموذج النصي هي الوقت الحالي الذي يتم فيه تحديث الحقل. |
| Calculated | `5` | يتم حساب قيمة حقل النموذج النصي من التعبير المحدد في the[`TextInputDefault`](../formfield/textinputdefault/) الملكية. |

## أمثلة

يوضح كيفية إنشاء حقول النموذج.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// حقول النموذج هي كائنات في المستند يمكن للمستخدم التفاعل معها من خلال مطالبته بإدخال القيم.
// يمكننا إنشاؤها باستخدام أداة إنشاء المستندات، وفيما يلي طريقتان للقيام بذلك.
// 1 - إدخال النص الأساسي:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - مربع تحرير وسرد يحتوي على نص موجه ونطاق من القيم المحتملة:
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
