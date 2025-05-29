---
title: DocumentBuilder.InsertCheckBox
linktitle: InsertCheckBox
articleTitle: InsertCheckBox
second_title: Aspose.Words لـ .NET
description: يمكنك بسهولة إضافة حقول نموذج مربع الاختيار التفاعلية باستخدام طريقة InsertCheckBox في DocumentBuilder، مما يعزز مشاركة المستخدم في مستنداتك.
type: docs
weight: 290
url: /ar/net/aspose.words/documentbuilder/insertcheckbox/
---
## InsertCheckBox(*string, bool, int*) {#insertcheckbox_1}

يقوم بإدراج حقل نموذج مربع الاختيار في الموضع الحالي.

```csharp
public FormField InsertCheckBox(string name, bool checkedValue, int size)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم حقل النموذج. يمكن أن يكون نصًا فارغًا. سيتم حذف أي قيمة أطول من ٢٠ حرفًا. |
| checkedValue | Boolean | تم التحقق من حالة حقل نموذج مربع الاختيار. |
| size | Int32 | يُحدِّد حجم مربع الاختيار بالنقاط. حدّد القيمة 0 لـ MS Word لحساب حجم مربع الاختيار تلقائيًا. |

### قيمة الإرجاع

عقدة حقل النموذج التي تم إدراجها للتو.

## ملاحظات

إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

## أمثلة

يوضح كيفية إدراج مربعات الاختيار في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج مربعات الاختيار ذات الأحجام المختلفة والحالات المحددة الافتراضية.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// تحتوي حقول النموذج على حد أقصى لطول الاسم يبلغ 20 حرفًا.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// يمكننا التفاعل مع مربعات الاختيار هذه في Microsoft Word عن طريق النقر المزدوج عليها.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### أنظر أيضا

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertCheckBox(*string, bool, bool, int*) {#insertcheckbox}

يقوم بإدراج حقل نموذج مربع الاختيار في الموضع الحالي.

```csharp
public FormField InsertCheckBox(string name, bool defaultValue, bool checkedValue, int size)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم حقل النموذج. يمكن أن يكون نصًا فارغًا. سيتم حذف أي قيمة أطول من ٢٠ حرفًا. |
| defaultValue | Boolean | القيمة الافتراضية لحقل نموذج مربع الاختيار. |
| checkedValue | Boolean | الحالة الحالية لفحص حقل نموذج مربع الاختيار. |
| size | Int32 | يُحدِّد حجم مربع الاختيار بالنقاط. حدّد القيمة 0 لـ MS Word لحساب حجم مربع الاختيار تلقائيًا. |

### قيمة الإرجاع

عقدة حقل النموذج التي تم إدراجها للتو.

## ملاحظات

إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

## أمثلة

يوضح كيفية إدراج مربعات الاختيار في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج مربعات الاختيار ذات الأحجام المختلفة والحالات المحددة الافتراضية.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// تحتوي حقول النموذج على حد أقصى لطول الاسم يبلغ 20 حرفًا.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// يمكننا التفاعل مع مربعات الاختيار هذه في Microsoft Word عن طريق النقر المزدوج عليها.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### أنظر أيضا

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
