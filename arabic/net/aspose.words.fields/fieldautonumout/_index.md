---
title: FieldAutoNumOut Class
linktitle: FieldAutoNumOut
articleTitle: FieldAutoNumOut
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldAutoNumOut لتنفيذ حقل AUTONUMOUT بسلاسة، مما يعزز أتمتة المستندات وكفاءتها.
type: docs
weight: 2010
url: /ar/net/aspose.words.fields/fieldautonumout/
---
## FieldAutoNumOut class

ينفذ حقل AUTONUMOUT.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldAutoNumOut : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldAutoNumOut](fieldautonumout/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | يُزيل الحقل من المستند. يُرجع عقدة بعد الحقل مباشرةً. إذا كانت نهاية الحقل هي آخر عقدة فرعية للعقدة الأصلية، تُرجع فقرته الأصلية. إذا كان الحقل قد حُذف مُسبقًا، تُرجع`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يُجري تحديث الحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | يُجري تحديثًا للحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |

## ملاحظات

يقوم بإدراج رقم تلقائي بتنسيق مخطط تفصيلي.

## أمثلة

يوضح كيفية ترقيم الفقرات باستخدام حقول AUTONUMOUT.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعرض حقول AUTONUMOUT رقمًا يتزايد عند كل حقل AUTONUMOUT.
// على عكس حقول AUTONUM، تستخدم حقول AUTONUMOUT مخطط ترقيم الخطوط العريضة،
// والذي يمكننا تعريفه في Microsoft Word عبر التنسيق -> النقاط والترقيم -> "مخطط رقمي".
// يسمح لنا هذا بترقيم العناصر تلقائيًا مثل القائمة المرقمة.
// حقول LISTNUM هي بديل أحدث لحقول AUTONUMOUT.
//سيعرض هذا الحقل "1".
builder.InsertField(FieldType.FieldAutoNumOutline, true);
builder.Writeln("\tParagraph 1.");

//سيعرض هذا الحقل "2".
builder.InsertField(FieldType.FieldAutoNumOutline, true);
builder.Writeln("\tParagraph 2.");

foreach (FieldAutoNumOut field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumOutline).ToList())
    Assert.AreEqual(" AUTONUMOUT ", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUMOUT.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
