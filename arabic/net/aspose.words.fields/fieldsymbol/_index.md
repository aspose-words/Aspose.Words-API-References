---
title: FieldSymbol Class
linktitle: FieldSymbol
articleTitle: FieldSymbol
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldSymbol لتنفيذ حقل SYMBOL بكفاءة، مما يعزز قدرات معالجة المستندات لديك.
type: docs
weight: 2870
url: /ar/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

ينفذ حقل الرمز.

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
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode/) { get; set; } | يحصل على قيمة نقطة رمز الحرف أو يعينها بالنظام العشري أو السداسي عشر. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing/) { get; set; } | يحصل على أو يعين ما إذا كان الحرف الذي تم استرداده بواسطة الحقل يؤثر على تباعد أسطر الفقرة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname/) { get; set; } | يحصل على اسم الخط الخاص بالحرف الذي تم استرداده بواسطة الحقل أو يعينه. |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize/) { get; set; } | يحصل على أو يعين حجم الخط بالنقاط للحرف الذي تم استرداده بواسطة الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi/) { get; set; } | يحصل على أو يحدد ما إذا كان يتم تفسير رمز الحرف كقيمة لحرف ANSI. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis/) { get; set; } | يحصل على أو يحدد ما إذا كان يتم تفسير رمز الحرف كقيمة لحرف SHIFT-JIS. |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode/) { get; set; } | يحصل على أو يحدد ما إذا كان يتم تفسير رمز الحرف كقيمة لحرف Unicode. |
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

يسترجع الحرف الذي تم تحديد قيمة نقطة الكود الخاصة به بالنظام العشري أو السداسي عشر.

## أمثلة

يوضح كيفية استخدام حقل الرمز.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث طرق لاستخدام حقل الرمز لعرض حرف واحد.
// 1 - أضف حقل رمز يعرض رمز © (حقوق الطبع والنشر)، المحدد بواسطة رمز حرف ANSI:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// رمز الحرف ANSI "U+00A9"، أو "169" في شكل عدد صحيح، مخصص لرمز حقوق النشر.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - أضف حقل رمز يعرض رمز ∞ (اللانهاية)، وقم بتعديل مظهره:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// في Unicode، يحتل رمز اللانهاية الكود "221E".
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// تغيير خط رمزنا بعد استخدام خريطة أحرف Windows
// للتأكد من أن الخط يمكنه تمثيل هذا الرمز.
field.FontName = "Calibri";
field.FontSize = "24";

// يمكننا تعيين هذا العلم للرموز الطويلة حتى لا تضغط على بقية النص الموجود على سطرها.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - أضف حقل الرمز الذي يعرض الحرف あ،
// مع الخط الذي يدعم صفحة أكواد Shift-JIS (Windows-932):
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
