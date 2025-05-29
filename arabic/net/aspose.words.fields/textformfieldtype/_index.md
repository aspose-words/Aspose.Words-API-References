---
title: TextFormFieldType Enum
linktitle: TextFormFieldType
articleTitle: TextFormFieldType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Fields.TextFormFieldType enum، الذي يحدد أنواعًا مختلفة من حقول نموذج النص لتحسين أتمتة المستندات وتخصيصها.
type: docs
weight: 3180
url: /ar/net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

يحدد نوع حقل نموذج النص.

```csharp
public enum TextFormFieldType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Regular | `0` | يمكن لحقل نموذج النص أن يحتوي على أي نص. |
| Number | `1` | لا يمكن لحقل نموذج النص أن يحتوي على أرقام فقط. |
| Date | `2` | لا يمكن لحقل نموذج النص أن يحتوي إلا على قيمة تاريخ صالحة. |
| CurrentDate | `3` | قيمة حقل نموذج النص هي التاريخ الحالي عندما يتم تحديث الحقل. |
| CurrentTime | `4` | قيمة حقل نموذج النص هي الوقت الحالي الذي يتم فيه تحديث الحقل. |
| Calculated | `5` | يتم حساب قيمة حقل نموذج النص من التعبير المحدد في [`TextInputDefault`](../formfield/textinputdefault/) الملكية. |

## أمثلة

يوضح كيفية إنشاء حقول النموذج.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// حقول النموذج هي كائنات في المستند يمكن للمستخدم التفاعل معها من خلال مطالبته بإدخال القيم.
// يمكننا إنشاؤها باستخدام منشئ المستندات، وفيما يلي طريقتان للقيام بذلك.
// 1 - إدخال النص الأساسي:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - مربع مشترك يحتوي على نص موجه ومجموعة من القيم المحتملة:
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
