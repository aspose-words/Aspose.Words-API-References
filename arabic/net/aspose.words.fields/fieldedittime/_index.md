---
title: FieldEditTime Class
linktitle: FieldEditTime
articleTitle: FieldEditTime
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.FieldEditTime فصل. ينفذ حقل EDITTIME في C#.
type: docs
weight: 1840
url: /ar/net/aspose.words.fields/fieldedittime/
---
## FieldEditTime class

ينفذ حقل EDITTIME.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldEditTime : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldEditTime](fieldedittime/)() | Default_Constructor |

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
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

## ملاحظات

استرداد إجمالي وقت التحرير، بالدقائق، منذ إنشاء المستند.

## أمثلة

يوضح كيفية استخدام حقل EDITTIME.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// سيظهر حقل EDITTIME، بالدقائق،
// الوقت المستغرق في فتح المستند في نافذة Microsoft Word.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("You've been editing this document for ");
FieldEditTime field = (FieldEditTime)builder.InsertField(FieldType.FieldEditTime, true);
builder.Writeln(" minutes.");

// خاصية الوثيقة المضمنة هذه تتتبع الدقائق. يستخدم Microsoft Word هذه الخاصية
// لتتبع الوقت الذي يقضيه المستند مفتوحًا. يمكننا أيضًا تعديله بأنفسنا.
doc.BuiltInDocumentProperties.TotalEditingTime = 10;
field.Update();

Assert.AreEqual(" EDITTIME ", field.GetFieldCode());
Assert.AreEqual("10", field.Result);

// لا يقوم الحقل بتحديث نفسه في الوقت الفعلي، ويجب أن يتم ذلك أيضًا
// يتم تحديثه يدويًا في Microsoft Word في أي وقت نحتاج فيه إلى قيمة دقيقة.
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.EDITTIME.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
