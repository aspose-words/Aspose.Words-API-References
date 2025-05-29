---
title: Paragraph.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words لـ .NET
description: أدرج الحقول في الفقرات بسهولة باستخدام طريقة Paragraph InsertField. حسّن أداء مستندك وسهّل إدارة محتواه.
type: docs
weight: 290
url: /ar/net/aspose.words/paragraph/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool, [Node](../../node/), bool*) {#insertfield}

يُدرج حقلاً في هذه الفقرة.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldType | FieldType | نوع الحقل الذي سيتم إدراجه. |
| updateField | Boolean | يحدد ما إذا كان سيتم تحديث الحقل على الفور. |
| refNode | Node | عقدة مرجعية داخل هذه الفقرة (إذا*refNode* يكون`باطل`(ثم يضاف إلى نهاية الفقرة). |
| isAfter | Boolean | ما إذا كان سيتم إدراج الحقل بعد أو قبل عقدة المرجع. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الكائن الذي يمثل الحقل المدرج.

## أمثلة

يُظهر طرقًا مختلفة لإضافة الحقول إلى فقرة.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإدراج حقل في فقرة.
// 1 - إدراج حقل المؤلف في فقرة بعد إحدى العقد الفرعية للفقرة:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - إدراج حقل اقتباس بعد إحدى العقد الفرعية للفقرة:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - إدراج حقل اقتباس قبل إحدى العقد الفرعية للفقرة،
// واحصل عليه لعرض قيمة عنصر نائب:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

//سيعرض هذا الحقل قيمة العنصر النائب الخاصة به حتى نقوم بتحديثه.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Node](../../node/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertField(*string, [Node](../../node/), bool*) {#insertfield_1}

يُدرج حقلاً في هذه الفقرة.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المراد إدراجه (بدون أقواس متعرجة). |
| refNode | Node | عقدة مرجعية داخل هذه الفقرة (إذا*refNode* يكون`باطل`(ثم يضاف إلى نهاية الفقرة). |
| isAfter | Boolean | ما إذا كان سيتم إدراج الحقل بعد أو قبل عقدة المرجع. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الكائن الذي يمثل الحقل المدرج.

## أمثلة

يُظهر طرقًا مختلفة لإضافة الحقول إلى فقرة.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإدراج حقل في فقرة.
// 1 - إدراج حقل المؤلف في فقرة بعد إحدى العقد الفرعية للفقرة:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - إدراج حقل اقتباس بعد إحدى العقد الفرعية للفقرة:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - إدراج حقل اقتباس قبل إحدى العقد الفرعية للفقرة،
// واحصل عليه لعرض قيمة عنصر نائب:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

//سيعرض هذا الحقل قيمة العنصر النائب الخاصة به حتى نقوم بتحديثه.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertField(*string, string, [Node](../../node/), bool*) {#insertfield_2}

يُدرج حقلاً في هذه الفقرة.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المراد إدراجه (بدون أقواس متعرجة). |
| fieldValue | String | قيمة الحقل المراد إدراجها. تمرير`باطل` للحقول التي لا تحتوي على قيمة. |
| refNode | Node | عقدة مرجعية داخل هذه الفقرة (إذا*refNode* يكون`باطل`(ثم يضاف إلى نهاية الفقرة). |
| isAfter | Boolean | ما إذا كان سيتم إدراج الحقل بعد أو قبل عقدة المرجع. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الكائن الذي يمثل الحقل المدرج.

## أمثلة

يُظهر طرقًا مختلفة لإضافة الحقول إلى فقرة.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// فيما يلي ثلاث طرق لإدراج حقل في فقرة.
// 1 - إدراج حقل المؤلف في فقرة بعد إحدى العقد الفرعية للفقرة:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - إدراج حقل اقتباس بعد إحدى العقد الفرعية للفقرة:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - إدراج حقل اقتباس قبل إحدى العقد الفرعية للفقرة،
// واحصل عليه لعرض قيمة عنصر نائب:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

//سيعرض هذا الحقل قيمة العنصر النائب الخاصة به حتى نقوم بتحديثه.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
