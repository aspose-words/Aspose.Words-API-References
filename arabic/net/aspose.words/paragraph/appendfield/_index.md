---
title: Paragraph.AppendField
linktitle: AppendField
articleTitle: AppendField
second_title: Aspose.Words لـ .NET
description: Paragraph AppendField طريقة. إلحاق حقل بهذه الفقرة في C#.
type: docs
weight: 240
url: /ar/net/aspose.words/paragraph/appendfield/
---
## AppendField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#appendfield}

إلحاق حقل بهذه الفقرة.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldType | FieldType | نوع الحقل المراد إلحاقه. |
| updateField | Boolean | يحدد ما إذا كان سيتم تحديث الحقل على الفور. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) كائن يمثل الحقل الملحق.

## أمثلة

يعرض طرقًا مختلفة لإلحاق الحقول بالفقرة.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإلحاق حقل بنهاية الفقرة.
// 1 - قم بإلحاق حقل التاريخ باستخدام نوع الحقل، ثم قم بتحديثه:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - إلحاق حقل الوقت باستخدام رمز الحقل:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - قم بإلحاق حقل عرض أسعار باستخدام رمز الحقل، واجعله يعرض قيمة عنصر نائب:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// سيعرض هذا الحقل قيمة العنصر النائب الخاص به حتى نقوم بتحديثه.
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

إلحاق حقل بهذه الفقرة.

```csharp
public Field AppendField(string fieldCode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المراد إلحاقه (بدون الأقواس المتعرجة). |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) كائن يمثل الحقل الملحق.

## أمثلة

يعرض طرقًا مختلفة لإلحاق الحقول بالفقرة.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإلحاق حقل بنهاية الفقرة.
// 1 - قم بإلحاق حقل التاريخ باستخدام نوع الحقل، ثم قم بتحديثه:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - إلحاق حقل الوقت باستخدام رمز الحقل:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - قم بإلحاق حقل عرض أسعار باستخدام رمز الحقل، واجعله يعرض قيمة عنصر نائب:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// سيعرض هذا الحقل قيمة العنصر النائب الخاص به حتى نقوم بتحديثه.
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

إلحاق حقل بهذه الفقرة.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المراد إلحاقه (بدون الأقواس المتعرجة). |
| fieldValue | String | قيمة الحقل المراد إلحاقه. يمر`باطل` للحقول التي ليس لها قيمة. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) كائن يمثل الحقل الملحق.

## أمثلة

يعرض طرقًا مختلفة لإلحاق الحقول بالفقرة.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإلحاق حقل بنهاية الفقرة.
// 1 - قم بإلحاق حقل التاريخ باستخدام نوع الحقل، ثم قم بتحديثه:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - إلحاق حقل الوقت باستخدام رمز الحقل:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - قم بإلحاق حقل عرض أسعار باستخدام رمز الحقل، واجعله يعرض قيمة عنصر نائب:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// سيعرض هذا الحقل قيمة العنصر النائب الخاص به حتى نقوم بتحديثه.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
