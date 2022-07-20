---
title: InsertField
second_title: Aspose.Words لمراجع .NET API
description: إدراج حقل في هذه الفقرة ._ x000d_
type: docs
weight: 270
url: /ar/net/aspose.words/paragraph/insertfield/
---
## InsertField(FieldType, bool, Node, bool) {#insertfield}

إدراج حقل في هذه الفقرة ._ x000d_

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldType | FieldType | نوع الحقل المراد إدراجه. |
| updateField | Boolean | يحدد ما إذا كان سيتم تحديث الحقل على الفور. |
| refNode | Node | العقدة المرجعية داخل هذه الفقرة (إذا كانت refNode فارغة ، فسيتم إلحاقها بنهاية الفقرة). |
| isAfter | Boolean | ما إذا كان سيتم إدراج الحقل بعد العقدة المرجعية أو قبلها. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field) كائن يمثل الحقل المدرج.

### أمثلة

يُظهر طرقًا مختلفة لإضافة الحقول إلى فقرة.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإدراج حقل في فقرة.
// 1 - أدخل حقل AUTHOR في فقرة بعد إحدى العقد الفرعية للفقرة:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - أدخل حقل QUOTE بعد إحدى العقد الفرعية للفقرة:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - أدخل حقل QUOTE قبل إحدى العقد الفرعية للفقرة ،
// واجعله يعرض قيمة عنصر نائب:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// سيعرض هذا الحقل قيمة العنصر النائب الخاص به حتى نقوم بتحديثه.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field)
* enum [FieldType](../../../aspose.words.fields/fieldtype)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* مساحة الاسم [Aspose.Words](../../paragraph)
* المجسم [Aspose.Words](../../../)

---

## InsertField(string, Node, bool) {#insertfield_1}

إدراج حقل في هذه الفقرة ._ x000d_

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المطلوب إدراجه (بدون الأقواس المتعرجة). |
| refNode | Node | العقدة المرجعية داخل هذه الفقرة (إذا كانت refNode فارغة ، فسيتم إلحاقها بنهاية الفقرة). |
| isAfter | Boolean | ما إذا كان سيتم إدراج الحقل بعد العقدة المرجعية أو قبلها. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field) كائن يمثل الحقل المدرج.

### أمثلة

يُظهر طرقًا مختلفة لإضافة الحقول إلى فقرة.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإدراج حقل في فقرة.
// 1 - أدخل حقل AUTHOR في فقرة بعد إحدى العقد الفرعية للفقرة:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - أدخل حقل QUOTE بعد إحدى العقد الفرعية للفقرة:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - أدخل حقل QUOTE قبل إحدى العقد الفرعية للفقرة ،
// واجعله يعرض قيمة عنصر نائب:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// سيعرض هذا الحقل قيمة العنصر النائب الخاص به حتى نقوم بتحديثه.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* مساحة الاسم [Aspose.Words](../../paragraph)
* المجسم [Aspose.Words](../../../)

---

## InsertField(string, string, Node, bool) {#insertfield_2}

إدراج حقل في هذه الفقرة ._ x000d_

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المطلوب إدراجه (بدون الأقواس المتعرجة). |
| fieldValue | String | قيمة الحقل المطلوب إدراجها. تمرير فارغ للحقول التي ليس لها قيمة. |
| refNode | Node | العقدة المرجعية داخل هذه الفقرة (إذا كانت refNode فارغة ، فسيتم إلحاقها بنهاية الفقرة). |
| isAfter | Boolean | ما إذا كان سيتم إدراج الحقل بعد العقدة المرجعية أو قبلها. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field) كائن يمثل الحقل المدرج.

### أمثلة

يُظهر طرقًا مختلفة لإضافة الحقول إلى فقرة.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإدراج حقل في فقرة.
// 1 - أدخل حقل AUTHOR في فقرة بعد إحدى العقد الفرعية للفقرة:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - أدخل حقل QUOTE بعد إحدى العقد الفرعية للفقرة:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - أدخل حقل QUOTE قبل إحدى العقد الفرعية للفقرة ،
// واجعله يعرض قيمة عنصر نائب:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// سيعرض هذا الحقل قيمة العنصر النائب الخاص به حتى نقوم بتحديثه.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* مساحة الاسم [Aspose.Words](../../paragraph)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
