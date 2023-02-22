---
title: Class FieldShape
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldShape فصل. تنفيذ حقل الشكل .
type: docs
weight: 2260
url: /ar/net/aspose.words.fields/fieldshape/
---
## FieldShape class

تنفيذ حقل الشكل .

```csharp
public class FieldShape : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldShape](fieldshape/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [Text](../../aspose.words.fields/fieldshape/text/) { get; set; } | الحصول على النص المراد استرداده أو تعيينه . |
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

استرداد النص المحدد.

### أمثلة

يوضح كيفية إنشاء قوائم متوافقة مع اللغة ذات الاتجاه من اليمين إلى اليسار باستخدام حقول BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فقرات أرقام الحقول BIDIOUTLINE مثل حقول AUTONUM / LISTNUM ،
// ولكنه يكون مرئيًا فقط عند تمكين لغة تحرير من اليمين إلى اليسار ، مثل العبرية أو العربية.
// سيعرض الحقل التالي ".1" ، المكافئ RTL لرقم القائمة "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// أضف حقلين BIDIOUTLINE آخرين ، والذي سيعرض ".2" و ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// اضبط محاذاة النص الأفقي لكل فقرة في المستند على RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// إذا قمنا بتمكين لغة تحرير من اليمين إلى اليسار في Microsoft Word ، فستعرض الحقول الخاصة بنا الأرقام.
// وإلا فسيتم عرض "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

يوضح كيفية معالجة بعض حقول Microsoft Word القديمة مثل SHAPE و EMBED أثناء التحميل.

```csharp
// افتح مستندًا تم إنشاؤه في Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// إذا فتحنا مستند Word وضغطنا على Alt + F9 ، فسنرى شكل وحقل EMBED.
// حقل الشكل هو نقطة الارتساء / قماش الرسم لكائن شكل تلقائي مع تمكين نمط التفاف "سطري مع النص".
// يحتوي حقل EMBED على نفس الوظيفة ، ولكن بالنسبة لكائن مضمن ،
// مثل جدول بيانات من مستند Excel خارجي.
// ومع ذلك ، لن تظهر هذه الحقول في مجموعة الحقول الخاصة بالمستند.
Assert.AreEqual(0, doc.Range.Fields.Count);

// تدعم الإصدارات القديمة من Microsoft Word هذه الحقول فقط.
// ستؤدي عملية تحميل المستند إلى تحويل هذه الحقول إلى كائنات شكل ،
// التي يمكننا الوصول إليها في مجموعة عقدة المستند.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// تتوافق عقدة الشكل الأولى مع حقل الشكل في مستند الإدخال ،
// وهي اللوحة القماشية المضمنة للشكل التلقائي.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// عقدة الشكل الثانية هي الشكل التلقائي نفسه.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// الشكل الثالث هو ما كان حقل EMBED الذي يحتوي على جدول البيانات الخارجي.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


