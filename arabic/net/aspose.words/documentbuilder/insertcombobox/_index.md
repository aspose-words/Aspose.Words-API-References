---
title: DocumentBuilder.InsertComboBox
linktitle: InsertComboBox
articleTitle: InsertComboBox
second_title: Aspose.Words لـ .NET
description: حسّن مستنداتك باستخدام طريقة InsertComboBox من DocumentBuilder. أضف بسهولة حقول نماذج تفاعلية من مربعات التحرير والسرد لتحسين تجربة المستخدم.
type: docs
weight: 300
url: /ar/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

يقوم بإدراج حقل نموذج المجموعة في الموضع الحالي.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم حقل النموذج. يمكن أن يكون نصًا فارغًا. سيتم حذف أي قيمة أطول من ٢٠ حرفًا. |
| items | String[] | عناصر المجموعة. الحد الأقصى ٢٥ عنصرًا. |
| selectedIndex | Int32 | فهرس العنصر المحدد في ComboBox. |

### قيمة الإرجاع

عقدة حقل النموذج التي تم إدراجها للتو.

## ملاحظات

إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

## أمثلة

يوضح كيفية إدراج حقل نموذج مربع المجموعة في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج نموذج يطالب المستخدم باختيار أحد العناصر من القائمة.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
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
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
