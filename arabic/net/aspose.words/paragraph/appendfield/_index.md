---
title: Paragraph.AppendField
linktitle: AppendField
articleTitle: AppendField
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستندك باستخدام طريقة Paragraph AppendField، من خلال إضافة حقول مخصصة إلى الفقرات بسلاسة لتحسين التنظيم والوضوح.
type: docs
weight: 260
url: /ar/net/aspose.words/paragraph/appendfield/
---
## AppendField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#appendfield}

يضيف حقلًا إلى هذه الفقرة.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldType | FieldType | نوع الحقل المراد إضافته. |
| updateField | Boolean | يحدد ما إذا كان سيتم تحديث الحقل على الفور. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الكائن الذي يمثل الحقل الملحق.

## أمثلة

يُظهر طرقًا مختلفة لإضافة الحقول إلى فقرة.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإضافة حقل إلى نهاية الفقرة.
// 1 - قم بإضافة حقل DATE باستخدام نوع الحقل، ثم قم بتحديثه:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - إضافة حقل الوقت باستخدام رمز الحقل:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - أضف حقل QUOTE باستخدام رمز الحقل، واجعله يعرض قيمة عنصر نائب:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

//سيعرض هذا الحقل قيمة العنصر النائب الخاصة به حتى نقوم بتحديثه.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## AppendField(*string*) {#appendfield_1}

يضيف حقلًا إلى هذه الفقرة.

```csharp
public Field AppendField(string fieldCode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المراد إضافته (بدون أقواس متعرجة). |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الكائن الذي يمثل الحقل الملحق.

## أمثلة

يُظهر طرقًا مختلفة لإضافة الحقول إلى فقرة.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإضافة حقل إلى نهاية الفقرة.
// 1 - قم بإضافة حقل DATE باستخدام نوع الحقل، ثم قم بتحديثه:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - إضافة حقل الوقت باستخدام رمز الحقل:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - أضف حقل QUOTE باستخدام رمز الحقل، واجعله يعرض قيمة عنصر نائب:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

//سيعرض هذا الحقل قيمة العنصر النائب الخاصة به حتى نقوم بتحديثه.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## AppendField(*string, string*) {#appendfield_2}

يضيف حقلًا إلى هذه الفقرة.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المراد إضافته (بدون أقواس متعرجة). |
| fieldValue | String | قيمة الحقل المراد إضافتها. تمرير`باطل` للحقول التي لا تحتوي على قيمة. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الكائن الذي يمثل الحقل الملحق.

## أمثلة

يُظهر طرقًا مختلفة لإضافة الحقول إلى فقرة.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإضافة حقل إلى نهاية الفقرة.
// 1 - قم بإضافة حقل DATE باستخدام نوع الحقل، ثم قم بتحديثه:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - إضافة حقل الوقت باستخدام رمز الحقل:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - أضف حقل QUOTE باستخدام رمز الحقل، واجعله يعرض قيمة عنصر نائب:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

//سيعرض هذا الحقل قيمة العنصر النائب الخاصة به حتى نقوم بتحديثه.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
