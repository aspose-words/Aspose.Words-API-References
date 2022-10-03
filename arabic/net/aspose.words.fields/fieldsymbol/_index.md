---
title: FieldSymbol
second_title: Aspose.Words لمراجع .NET API
description: تنفيذ حقل SYMBOL .
type: docs
weight: 2310
url: /ar/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

تنفيذ حقل SYMBOL .

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
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode/) { get; set; } | الحصول على أو تعيين قيمة نقطة رمز الحرف في النظام العشري أو الست عشري. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing/) { get; set; } | الحصول على أو تحديد ما إذا كان الحرف الذي تم استرداده بواسطة الحقل يؤثر على تباعد الأسطر في الفقرة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname/) { get; set; } | الحصول على أو تحديد اسم خط الحرف الذي تم استرداده بواسطة الحقل. |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize/) { get; set; } | الحصول على أو تحديد الحجم بالنقاط الخاصة بخط الحرف الذي تم استرجاعه بواسطة الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi/) { get; set; } | الحصول على أو تحديد ما إذا كان يتم تفسير رمز الحرف كقيمة لحرف ANSI. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis/) { get; set; } | الحصول على أو تحديد ما إذا كان يتم تفسير رمز الحرف كقيمة لحرف SHIFT-JIS. |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode/) { get; set; } | الحصول على أو تحديد ما إذا كان يتم تفسير رمز الحرف كقيمة لحرف Unicode. |
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

استرداد الحرف الذي تم تحديد قيمة نقطة الكود الخاصة به في النظام العشري أو الست عشري.

### أمثلة

يوضح كيفية استخدام حقل SYMBOL.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث طرق لاستخدام حقل SYMBOL لعرض حرف واحد.
// 1 - أضف حقل SYMBOL الذي يعرض رمز © (حقوق النشر) المحدد بواسطة رمز حرف ANSI:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// رمز حرف ANSI "U + 00A9" أو "169" في شكل عدد صحيح محجوز لرمز حقوق النشر.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - أضف حقل SYMBOL الذي يعرض الرمز ∞ (اللانهاية) ، وقم بتعديل مظهره:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// في Unicode ، يحتل رمز اللانهاية الكود "221E".
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// تغيير خط رمزنا بعد استخدام مخطط توزيع الأحرف في Windows
// للتأكد من أن الخط يمكن أن يمثل هذا الرمز.
field.FontName = "Calibri";
field.FontSize = "24";

// يمكننا تعيين هذا العلم للرموز الطويلة حتى لا يدفعوا بقية النص لأسفل على السطر.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - أضف حقل SYMBOL الذي يعرض الحرف ،
// بخط يدعم صفحة الترميز اللغوي Shift-JIS (Windows-932):
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
