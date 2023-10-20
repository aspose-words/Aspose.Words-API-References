---
title: DocumentBuilder.InsertCheckBox
linktitle: InsertCheckBox
articleTitle: InsertCheckBox
second_title: Aspose.Words لـ .NET
description: DocumentBuilder InsertCheckBox طريقة. إدراج حقل نموذج خانة الاختيار في الموضع الحالي في C#.
type: docs
weight: 290
url: /ar/net/aspose.words/documentbuilder/insertcheckbox/
---
## InsertCheckBox(*string, bool, int*) {#insertcheckbox_1}

إدراج حقل نموذج خانة الاختيار في الموضع الحالي.

```csharp
public FormField InsertCheckBox(string name, bool checkedValue, int size)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم حقل النموذج. يمكن أن تكون سلسلة فارغة. سيتم اقتطاع القيمة الأطول من 20 حرفًا. |
| checkedValue | Boolean | تم التحقق من حالة حقل نموذج خانة الاختيار. |
| size | Int32 | يحدد حجم مربع الاختيار بالنقاط. حدد 0 لـ MS Word لحساب حجم مربع الاختيار تلقائيًا. |

### قيمة الإرجاع

عقدة حقل النموذج التي تم إدراجها للتو.

## ملاحظات

إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

## أمثلة

يوضح كيفية إدراج خانات الاختيار في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج مربعات اختيار بأحجام مختلفة وحالات التحقق الافتراضية.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// حقول النموذج لها حد أقصى لطول الاسم يبلغ 20 حرفًا.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// يمكننا التفاعل مع مربعات الاختيار هذه في Microsoft Word بالنقر المزدوج عليها.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### أنظر أيضا

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertCheckBox(*string, bool, bool, int*) {#insertcheckbox}

إدراج حقل نموذج خانة الاختيار في الموضع الحالي.

```csharp
public FormField InsertCheckBox(string name, bool defaultValue, bool checkedValue, int size)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم حقل النموذج. يمكن أن تكون سلسلة فارغة. سيتم اقتطاع القيمة الأطول من 20 حرفًا. |
| defaultValue | Boolean | القيمة الافتراضية لحقل نموذج خانة الاختيار. |
| checkedValue | Boolean | الحالة الحالية المحددة لحقل نموذج خانة الاختيار. |
| size | Int32 | يحدد حجم مربع الاختيار بالنقاط. حدد 0 لـ MS Word لحساب حجم مربع الاختيار تلقائيًا. |

### قيمة الإرجاع

عقدة حقل النموذج التي تم إدراجها للتو.

## ملاحظات

إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

## أمثلة

يوضح كيفية إدراج خانات الاختيار في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج مربعات اختيار بأحجام مختلفة وحالات التحقق الافتراضية.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// حقول النموذج لها حد أقصى لطول الاسم يبلغ 20 حرفًا.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// يمكننا التفاعل مع مربعات الاختيار هذه في Microsoft Word بالنقر المزدوج عليها.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### أنظر أيضا

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
