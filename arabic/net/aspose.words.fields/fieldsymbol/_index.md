---
title: Class FieldSymbol
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldSymbol فصل. ينفذ حقل SYMBOL.
type: docs
weight: 2460
url: /ar/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

ينفذ حقل SYMBOL.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldSymbol : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldSymbol](fieldsymbol/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode/) { get; set; } | الحصول على قيمة نقطة رمز الحرف أو تعيينها بالنظام العشري أو الست عشري. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing/) { get; set; } | الحصول على أو تعيين ما إذا كان الحرف الذي يتم استرداده بواسطة الحقل يؤثر على تباعد الأسطر في الفقرة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname/) { get; set; } | الحصول على أو تعيين اسم خط الحرف الذي تم استرداده بواسطة الحقل. |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize/) { get; set; } | الحصول على أو تعيين الحجم بنقاط خط الحرف الذي تم استرداده بواسطة الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تفسير رمز الحرف كقيمة حرف ANSI. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تفسير رمز الحرف كقيمة حرف SHIFT-JIS. |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تفسير رمز الحرف كقيمة حرف Unicode. |
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

استرداد الحرف الذي تم تحديد قيمة نقطة الرمز الخاصة به بالنظام العشري أو الست عشري.

### أمثلة

يوضح كيفية استخدام حقل الرمز.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث طرق لاستخدام حقل الرمز لعرض حرف واحد.
// 1 - أضف حقل SYMBOL الذي يعرض رمز © (حقوق الطبع والنشر)، المحدد بواسطة رمز حرف ANSI:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// رمز حرف ANSI "U+00A9"، أو "169" في شكل عدد صحيح، محجوز لرمز حقوق الطبع والنشر.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - أضف حقل SYMBOL الذي يعرض رمز ∞ (اللانهاية) وتعديل مظهره:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// في Unicode، يحتل رمز اللانهاية الرمز "221E".
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// قم بتغيير خط الرمز الخاص بنا بعد استخدام Windows Character Map
// للتأكد من أن الخط يمكن أن يمثل هذا الرمز.
field.FontName = "Calibri";
field.FontSize = "24";

// يمكننا تعيين هذه العلامة للرموز الطويلة حتى لا تدفع بقية النص الموجود على سطرها للأسفل.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - أضف حقل SYMBOL الذي يعرض الحرف あ،
// بخط يدعم صفحة الرموز Shift-JIS (Windows-932):
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);
field.FontName = "MS Gothic";
field.CharacterCode = 0x82A0.ToString();
field.IsShiftJis = true;

Assert.AreEqual(" SYMBOL  33440 \\f \"MS Gothic\" \\j", field.GetFieldCode());

builder.Write("Line 3");

doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


