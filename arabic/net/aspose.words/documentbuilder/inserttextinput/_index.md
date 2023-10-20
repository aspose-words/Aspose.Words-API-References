---
title: DocumentBuilder.InsertTextInput
linktitle: InsertTextInput
articleTitle: InsertTextInput
second_title: Aspose.Words لـ .NET
description: DocumentBuilder InsertTextInput طريقة. إدراج حقل نموذج نصي في الموضع الحالي في C#.
type: docs
weight: 470
url: /ar/net/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder.InsertTextInput method

إدراج حقل نموذج نصي في الموضع الحالي.

```csharp
public FormField InsertTextInput(string name, TextFormFieldType type, string format, 
    string fieldValue, int maxLength)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم حقل النموذج. يمكن أن تكون سلسلة فارغة. |
| type | TextFormFieldType | يحدد نوع حقل النموذج النصي. |
| format | String | سلسلة التنسيق المستخدمة لتنسيق قيمة حقل النموذج. |
| fieldValue | String | النص الذي سيتم عرضه في هذا المجال. |
| maxLength | Int32 | الحد الأقصى للطول الذي يمكن للمستخدم إدخاله في حقل النموذج. اضبط على الصفر لمدة غير محدودة. |

### قيمة الإرجاع

عقدة حقل النموذج التي تم إدراجها للتو.

## ملاحظات

إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

## أمثلة

يوضح كيفية إدراج حقل نموذج إدخال نص في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل نموذجًا يطالب المستخدم بإدخال النص.
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

يوضح كيفية إدراج حقل نموذج إدخال النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// أدخل حقل إدخال النص، والذي سيسمح للمستخدم بالنقر فوقه وإدخال النص.
// قم بتعيين بعض نص العنصر النائب الذي يمكن للمستخدم الكتابة فوقه وتمريره
// الحد الأقصى لطول النص هو 0 لتطبيق أي حد على محتويات حقل النموذج.
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// سيظهر حقل النموذج على شكل علامة html "إدخال"، بنوع "نص".
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
```

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

* class [FormField](../../../aspose.words.fields/formfield/)
* enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
