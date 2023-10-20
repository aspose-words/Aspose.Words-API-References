---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.Field فصل. يمثل حقل مستند Microsoft Word في C#.
type: docs
weight: 1510
url: /ar/net/aspose.words.fields/field/
---
## Field class

يمثل حقل مستند Microsoft Word.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class Field
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/#update)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

## ملاحظات

الحقل في مستند Word عبارة عن بنية معقدة تتكون من عقد متعددة تتضمن بداية الحقل ورمز الحقل وفاصل الحقل ونتيجة الحقل ونهاية الحقل. يمكن أن تكون الحقول متداخلة، وتحتوي على محتوى غني وتمتد إلى فقرات أو أقسام متعددة في المستند. ال`Field` الفئة هي كائن "واجهة" يوفر خصائص وأساليب تسمح بالعمل مع الحقل ككائن واحد.

ال[`Start`](./start/) ,[`Separator`](./separator/) و[`End`](./end/) تشير الخصائص إلى بداية الحقل والعقد الفاصلة والنهاية للحقل على التوالي.

المحتوى بين بداية الحقل والفاصل هو رمز الحقل. المحتوى بين فاصل الحقل ونهاية الحقل هو نتيجة الحقل. يتكون رمز الحقل عادةً من واحد أو أكثر [`Run`](../../aspose.words/run/) الكائنات التي تحدد التعليمات. من المتوقع أن يقوم تطبيق المعالجة بتنفيذ رمز الحقل لحساب نتيجة الحقل.

تسمى عملية حساب النتائج الميدانية بالتحديث الميداني. يمكن لـ Aspose.Words تحديث نتائج field لمعظم أنواع الحقول بنفس الطريقة التي يقوم بها Microsoft Word. وأبرزها، Aspose.Words يمكنه حساب نتائج حتى حقول الصيغة الأكثر تعقيدًا. لحساب نتيجة field لحقل واحد استخدم[`Update`](./update/) طريقة. لتحديث الحقول في استخدام document بأكمله[`UpdateFields`](../../aspose.words/document/updatefields/).

يمكنك الحصول على نسخة النص العادي من رمز الحقل باستخدام[`GetFieldCode`](./getfieldcode/) الطريقة. يمكنك الحصول على إصدار النص العادي لنتيجة الحقل وتعيينه باستخدام[`Result`](./result/) property. يمكن أن يحتوي كل من رمز الحقل ونتيجة الحقل على محتوى معقد، مثل الحقول المتداخلة والفقرات والأشكال وجداول وفي هذه الحالة قد ترغب في العمل مع عقد الحقل مباشرة إذا كنت بحاجة إلى مزيد من التحكم.

لا تقم بإنشاء مثيلات لـ`Field` class مباشرة. لإنشاء حقل جديد استخدم[`InsertField`](../../aspose.words/documentbuilder/insertfield/) طريقة.

## أمثلة

يوضح كيفية إدراج حقل في مستند باستخدام رمز الحقل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// هذا التحميل الزائد لطريقة InsertField يقوم تلقائيًا بتحديث الحقول المدرجة.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
