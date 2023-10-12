---
title: Class FieldAuthor
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldAuthor فصل. ينفذ حقل المؤلف.
type: docs
weight: 1570
url: /ar/net/aspose.words.fields/fieldauthor/
---
## FieldAuthor class

ينفذ حقل المؤلف.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldAuthor : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldAuthor](fieldauthor/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AuthorName](../../aspose.words.fields/fieldauthor/authorname/) { get; set; } | الحصول على اسم مؤلف المستند أو تعيينه. |
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
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

استرداد وتعيين اسم مؤلف المستند اختياريًا، كما هو مسجل في **مؤلف** خاصية خصائص المستند المضمنة.

### أمثلة

يوضح كيفية استخدام حقل المؤلف لعرض اسم منشئ المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حقول المؤلف مصدر نتائجها من خاصية المستند المضمنة والتي تسمى "المؤلف".
// إذا قمنا بإنشاء مستند وحفظه في برنامج Microsoft Word،
// سيكون له اسم المستخدم الخاص بنا في تلك الخاصية.
// ومع ذلك، إذا قمنا بإنشاء مستند برمجيًا باستخدام Aspose.Words،
// ستكون خاصية "المؤلف" سلسلة فارغة بشكل افتراضي.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// قم بتعيين اسم مؤلف احتياطي لحقول المؤلف لاستخدامها
// إذا كانت خاصية "المؤلف" تحتوي على سلسلة فارغة.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// تحديث حقل المؤلف الذي يحتوي على قيمة
// سيتم تطبيق هذه القيمة على خاصية "المؤلف" المضمنة.
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// سيؤدي تغيير هذه الخاصية ثم تحديث حقل المؤلف إلى تطبيق هذه القيمة على الحقل.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// إذا قمنا بتحديث حقل المؤلف بعد تغيير خاصية "الاسم" الخاصة به،
// ثم سيعرض الحقل الاسم الجديد ويطبق الاسم الجديد على الخاصية المضمنة.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// حقول المؤلف لا تؤثر على خاصية DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


