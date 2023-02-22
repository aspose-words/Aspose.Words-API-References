---
title: Class FieldAuthor
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldAuthor فصل. تنفيذ حقل AUTHOR .
type: docs
weight: 1420
url: /ar/net/aspose.words.fields/fieldauthor/
---
## FieldAuthor class

تنفيذ حقل AUTHOR .

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
| [AuthorName](../../aspose.words.fields/fieldauthor/authorname/) { get; set; } | الحصول على أو تحديد اسم مؤلف المستند. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove/)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

استرداد ، واختيار اسم مؤلف المستند ، كما هو مسجل في ملف **مؤلف**خاصية the خصائص المستند المضمنة .

### أمثلة

يوضح كيفية استخدام حقل AUTHOR لعرض اسم منشئ المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// مصدر الحقول AUTHOR هو نتائجها من خاصية المستند المضمنة التي تسمى "المؤلف".
// إذا أنشأنا مستندًا وحفظناه في Microsoft Word ،
// سيكون لها اسم المستخدم الخاص بنا في تلك الخاصية.
// ومع ذلك ، إذا أنشأنا مستندًا برمجيًا باستخدام Aspose.Words ،
 // ستكون خاصية "المؤلف" ، افتراضيًا ، سلسلة فارغة.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// تعيين اسم مؤلف احتياطي لحقول AUTHOR المراد استخدامها
// إذا كانت خاصية "المؤلف" تحتوي على سلسلة فارغة.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// تحديث حقل AUTHOR يحتوي على قيمة
// سيطبق هذه القيمة على خاصية "المؤلف" المضمنة.
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// سيؤدي تغيير هذه الخاصية ، ثم تحديث حقل AUTHOR إلى تطبيق هذه القيمة على الحقل.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// إذا قمنا بتحديث حقل AUTHOR بعد تغيير خاصية "الاسم" الخاصة به ،
// ثم سيعرض الحقل الاسم الجديد ويطبق الاسم الجديد على الخاصية المضمنة.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// لا تؤثر حقول AUTHOR على خاصية DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


