---
title: FieldEmbed Class
linktitle: FieldEmbed
articleTitle: FieldEmbed
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldEmbed لتنفيذ حقل EMBED بسلاسة، مما يعزز وظائف المستند وتنوعه.
type: docs
weight: 2260
url: /ar/net/aspose.words.fields/fieldembed/
---
## FieldEmbed class

ينفذ حقل EMBED.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldEmbed : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldEmbed](fieldembed/)() | Default_Constructor |

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

## أمثلة

يوضح كيفية التعامل مع بعض حقول Microsoft Word القديمة مثل SHAPE وEMBED أثناء التحميل.

```csharp
// افتح مستندًا تم إنشاؤه في Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// إذا فتحنا مستند Word وضغطنا على Alt+F9، فسنرى حقل SHAPE وحقل EMBED.
// حقل الشكل هو المرساة/اللوحة القماشية لكائن الشكل التلقائي مع تمكين نمط الالتفاف "متوافق مع النص".
// حقل EMBED له نفس الوظيفة، ولكن بالنسبة للكائن المضمن،
// مثل جدول بيانات من مستند Excel خارجي.
// ومع ذلك، لن تظهر هذه الحقول في مجموعة الحقول الخاصة بالمستند.
Assert.AreEqual(0, doc.Range.Fields.Count);

// هذه الحقول مدعومة فقط بواسطة الإصدارات القديمة من Microsoft Word.
// ستعمل عملية تحميل المستند على تحويل هذه الحقول إلى كائنات شكلية،
// والتي يمكننا الوصول إليها في مجموعة عقد المستند.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// تتوافق عقدة الشكل الأولى مع حقل الشكل في المستند المدخل،
// وهو القماش المضمن للشكل التلقائي.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// عقدة الشكل الثانية هي الشكل التلقائي نفسه.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// الشكل الثالث هو الحقل EMBED الذي يحتوي على جدول البيانات الخارجي.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
