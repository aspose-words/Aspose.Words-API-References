---
title: FieldTime Class
linktitle: FieldTime
articleTitle: FieldTime
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldTime لتطبيق سلس لحقل الوقت. حسّن أتمتة مستنداتك بميزات فعّالة!
type: docs
weight: 2910
url: /ar/net/aspose.words.fields/fieldtime/
---
## FieldTime class

ينفذ حقل الوقت.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldTime : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldTime](fieldtime/)() | Default_Constructor |

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

يقوم بإدراج التاريخ والوقت الحاليين.

## أمثلة

يوضح كيفية عرض الوقت الحالي باستخدام حقل الوقت.

```csharp
public void FieldTime()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // بشكل افتراضي، يتم عرض الوقت بتنسيق "س:د ص/م".
    FieldTime field = InsertFieldTime(builder, "");

    Assert.AreEqual(" TIME ", field.GetFieldCode());

    //يمكننا استخدام العلم \@ لتغيير تنسيق الوقت المعروض لدينا.
    field = InsertFieldTime(builder, "\\@ HHmm");

    Assert.AreEqual(" TIME \\@ HHmm", field.GetFieldCode());

    // يمكننا تعديل التنسيق للحصول على حقل الوقت لعرض التاريخ أيضًا، وفقًا للتقويم الميلادي.
    field = InsertFieldTime(builder, "\\@ \"M/d/yyyy h mm:ss am/pm\"");

    Assert.AreEqual(" TIME \\@ \"M/d/yyyy h mm:ss am/pm\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.TIME.docx");
}

/// <summary>
/// استخدم منشئ المستندات لإدراج حقل الوقت، وإدراج فقرة جديدة وإرجاع الحقل.
/// </summary>
private static FieldTime InsertFieldTime(DocumentBuilder builder, string format)
{
    FieldTime field = (FieldTime)builder.InsertField(FieldType.FieldTime, true);
    builder.MoveTo(field.Separator);
    builder.Write(format);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
