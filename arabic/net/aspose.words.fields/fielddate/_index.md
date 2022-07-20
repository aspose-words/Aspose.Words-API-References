---
title: FieldDate
second_title: Aspose.Words لمراجع .NET API
description: تنفذ حقل التاريخ ._ x000d_
type: docs
weight: 1620
url: /ar/net/aspose.words.fields/fielddate/
---
## FieldDate class

تنفذ حقل التاريخ ._ x000d_

```csharp
public class FieldDate : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldDate](fielddate)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format) { get; } | يحصل على أ[`FieldFormat`](../fieldformat) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | يحصل على نوع حقل Microsoft Word . |
| [UseLastFormat](../../aspose.words.fields/fielddate/uselastformat) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم استخدام تنسيق تم استخدامه مؤخرًا بواسطة تطبيق الاستضافة عند إدراج حقل DATE جديد. |
| [UseLunarCalendar](../../aspose.words.fields/fielddate/uselunarcalendar) { get; set; } | يحصل أو يحدد ما إذا كان سيتم استخدام التقويم الهجري القمري أو التقويم القمري العبري. |
| [UseSakaEraCalendar](../../aspose.words.fields/fielddate/usesakaeracalendar) { get; set; } | يحصل أو يحدد ما إذا كان سيتم استخدام تقويم Saka Era . |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fielddate/useumalquracalendar) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم استخدام تقويم أم القرى. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) ._ x000d_ يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) ._ x000d_ |
| [Remove](../../aspose.words.fields/field/remove)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

لإدراج التاريخ والوقت الحاليين. بشكل افتراضي ، يتم استخدام التقويم الميلادي.

### أمثلة

يوضح كيفية استخدام حقول التاريخ لعرض التواريخ وفقًا لأنواع التقويمات المختلفة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا أردنا دائمًا أن يعرض النص الموجود في المستند التاريخ الصحيح ، فيمكننا استخدام حقل التاريخ.
// فيما يلي ثلاثة أنواع من التقاويم الثقافية التي يمكن أن يستخدمها حقل التاريخ لعرض التاريخ.
// 1 - التقويم القمري الإسلامي:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - تقويم أم القرى:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - التقويم الوطني الهندي:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// أدخل حقل التاريخ وقم بتعيين نوع التقويم الخاص به على آخر نوع استخدمه التطبيق المضيف.
// في Microsoft Word ، سيكون النوع هو الأحدث استخدامًا في Insert - > نص - >. مربع حوار التاريخ والوقت.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### أنظر أيضا

* class [Field](../field)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->