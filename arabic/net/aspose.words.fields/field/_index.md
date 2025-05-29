---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.Field، مفتاحك لتحسين مستندات Microsoft Word باستخدام الحقول الديناميكية لتحسين الوظائف والكفاءة.
type: docs
weight: 1920
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
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | يُزيل الحقل من المستند. يُرجع عقدة بعد الحقل مباشرةً. إذا كانت نهاية الحقل هي آخر عقدة فرعية للعقدة الأصلية، تُرجع فقرته الأصلية. إذا كان الحقل قد حُذف مُسبقًا، تُرجع`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/#update)() | يُجري تحديث الحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | يُجري تحديثًا للحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |

## ملاحظات

الحقل في مستند وورد هو بنية معقدة تتكون من عدة عقد تتضمن بداية الحقل، ورمز الحقل، وفاصل الحقل، ونتيجة الحقل، ونهايته. يمكن أن تكون الحقول متداخلة، وتحتوي على محتوى غني، وتمتد إلى عدة فقرات أو أقسام في المستند.`Field` الفئة هي كائن "واجهة" يوفر خصائص وطرقًا تسمح بالعمل مع الحقل ككائن واحد.

ال[`Start`](./start/) ،[`Separator`](./separator/) و[`End`](./end/) تشير الخصائص إلى عقد البداية والفاصل والنهاية لحقل على التوالي.

المحتوى بين بداية الحقل والفاصل هو رمز الحقل. المحتوى بين فاصل الحقل ونهايته هو نتيجة الحقل. يتكون رمز الحقل عادةً من رمز واحد أو أكثر من .[`Run`](../../aspose.words/run/) الكائنات التي تحدد التعليمات. من المتوقع أن يقوم تطبيق المعالجة بتنفيذ رمز الحقل لحساب نتيجة الحقل.

تُسمى عملية حساب نتائج الحقول "تحديث الحقل". يُمكن لبرنامج Aspose.Words تحديث نتائج field لمعظم أنواع الحقول بنفس طريقة مايكروسوفت وورد. والجدير بالذكر أن Aspose.Words يستطيع حساب نتائج حتى حقول الصيغ الأكثر تعقيدًا. لحساب نتيجة field لحقل واحد، استخدم[`Update`](./update/) الطريقة. لتحديث الحقول في المستند بأكمله استخدم[`UpdateFields`](../../aspose.words/document/updatefields/).

يمكنك الحصول على نسخة النص العادي من رمز الحقل باستخدام[`GetFieldCode`](./getfieldcode/)الطريقة. يمكنك الحصول على إصدار النص العادي لنتيجة الحقل وتعيينه باستخدام[`Result`](./result/) يمكن أن يحتوي كل من رمز الحقل ونتيجة الحقل على محتوى معقد، مثل الحقول المتداخلة والفقرات والأشكال والجداول، وفي هذه الحالة قد ترغب في العمل مع عقد الحقل بشكل مباشر إذا كنت بحاجة إلى مزيد من التحكم.

لا تقم بإنشاء حالات من`Field` الفئة مباشرة. لإنشاء حقل جديد استخدم[`InsertField`](../../aspose.words/documentbuilder/insertfield/) طريقة.

## أمثلة

يوضح كيفية إدراج حقل في مستند باستخدام رمز الحقل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// يؤدي هذا التحميل الزائد لطريقة InsertField إلى تحديث الحقول المدرجة تلقائيًا.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
