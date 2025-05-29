---
title: DocumentBuilder.InsertTextInput
linktitle: InsertTextInput
articleTitle: InsertTextInput
second_title: Aspose.Words لـ .NET
description: أضف حقول نماذج النصوص بسهولة باستخدام طريقة InsertTextInput في DocumentBuilder. حسّن تجربة المستخدم وتفاعلية مستندك اليوم!
type: docs
weight: 510
url: /ar/net/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder.InsertTextInput method

يقوم بإدراج حقل نموذج نصي في الموضع الحالي.

```csharp
public FormField InsertTextInput(string name, TextFormFieldType type, string format, 
    string fieldValue, int maxLength)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم حقل النموذج. يمكن أن يكون سلسلة فارغة. |
| type | TextFormFieldType | يحدد نوع حقل نموذج النص. |
| format | String | سلسلة التنسيق المستخدمة لتنسيق قيمة حقل النموذج. |
| fieldValue | String | النص الذي سيتم عرضه في الحقل. |
| maxLength | Int32 | أقصى طول يُمكن للمستخدم إدخاله في حقل النموذج. اضبطه على صفر لطول غير محدود. |

### قيمة الإرجاع

عقدة حقل النموذج التي تم إدراجها للتو.

## ملاحظات

إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

## أمثلة

يوضح كيفية إدراج حقل نموذج إدخال النص في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج نموذج يطالب المستخدم بإدخال النص.
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

يوضح كيفية إدراج حقل نموذج إدخال النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// أدخل حقل إدخال نص، والذي سيسمح للمستخدم بالنقر فوقه وإدخال النص.
// تعيين بعض النصوص المؤقتة التي يمكن للمستخدم الكتابة فوقها وتمريرها
// الحد الأقصى لطول النص هو 0 لعدم تطبيق أي حد على محتويات حقل النموذج.
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// سيظهر حقل النموذج في شكل علامة HTML "إدخال"، مع نوع "نص".
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
```

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

* class [FormField](../../../aspose.words.fields/formfield/)
* enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
