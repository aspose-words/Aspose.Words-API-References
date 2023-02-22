---
title: Paragraph.AppendField
second_title: Aspose.Words لمراجع .NET API
description: Paragraph طريقة. لإلحاق حقل بهذه الفقرة .
type: docs
weight: 240
url: /ar/net/aspose.words/paragraph/appendfield/
---
## AppendField(FieldType, bool) {#appendfield}

لإلحاق حقل بهذه الفقرة .

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldType | FieldType | نوع الحقل المطلوب إلحاقه. |
| updateField | Boolean | يحدد ما إذا كان سيتم تحديث الحقل على الفور. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الذي يمثل الحقل الملحق.

### أمثلة

يُظهر طرقًا مختلفة لإلحاق الحقول بفقرة.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإلحاق حقل بنهاية فقرة.
// 1 - قم بإلحاق حقل التاريخ باستخدام نوع الحقل ، ثم قم بتحديثه:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - قم بإلحاق حقل TIME باستخدام رمز الحقل: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - قم بإلحاق حقل QUOTE باستخدام رمز الحقل ، واحصل عليه لعرض قيمة العنصر النائب:
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
* مساحة الاسم [Aspose.Words](../../paragraph/)
* المجسم [Aspose.Words](../../../)

---

## AppendField(string) {#appendfield_1}

لإلحاق حقل بهذه الفقرة .

```csharp
public Field AppendField(string fieldCode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المطلوب إلحاقه (بدون الأقواس المتعرجة). |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الذي يمثل الحقل الملحق.

### أمثلة

يُظهر طرقًا مختلفة لإلحاق الحقول بفقرة.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإلحاق حقل بنهاية فقرة.
// 1 - قم بإلحاق حقل التاريخ باستخدام نوع الحقل ، ثم قم بتحديثه:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - قم بإلحاق حقل TIME باستخدام رمز الحقل: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - قم بإلحاق حقل QUOTE باستخدام رمز الحقل ، واحصل عليه لعرض قيمة العنصر النائب:
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
* مساحة الاسم [Aspose.Words](../../paragraph/)
* المجسم [Aspose.Words](../../../)

---

## AppendField(string, string) {#appendfield_2}

لإلحاق حقل بهذه الفقرة .

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المطلوب إلحاقه (بدون الأقواس المتعرجة). |
| fieldValue | String | قيمة الحقل المطلوب إلحاقها. تمرير فارغ للحقول التي ليس لها قيمة. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الذي يمثل الحقل الملحق.

### أمثلة

يُظهر طرقًا مختلفة لإلحاق الحقول بفقرة.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإلحاق حقل بنهاية فقرة.
// 1 - قم بإلحاق حقل التاريخ باستخدام نوع الحقل ، ثم قم بتحديثه:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - قم بإلحاق حقل TIME باستخدام رمز الحقل: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - قم بإلحاق حقل QUOTE باستخدام رمز الحقل ، واحصل عليه لعرض قيمة العنصر النائب:
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
* مساحة الاسم [Aspose.Words](../../paragraph/)
* المجسم [Aspose.Words](../../../)


