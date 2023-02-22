---
title: Class FieldDisplayBarcode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldDisplayBarcode فصل. تنفذ حقل DISPLAYBARCODE .
type: docs
weight: 1650
url: /ar/net/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class

تنفذ حقل DISPLAYBARCODE .

```csharp
public class FieldDisplayBarcode : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldDisplayBarcode](fielddisplaybarcode/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/fielddisplaybarcode/addstartstopchar/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إضافة أحرف بدء / إيقاف لأنواع الباركود NW7 و CODE39. |
| [BackgroundColor](../../aspose.words.fields/fielddisplaybarcode/backgroundcolor/) { get; set; } | الحصول على أو تحديد لون خلفية رمز الباركود. القيم الصالحة موجودة في النطاق [0 ، 0xFFFFFF] |
| [BarcodeType](../../aspose.words.fields/fielddisplaybarcode/barcodetype/) { get; set; } | الحصول على نوع الرمز الشريطي أو تعيينه (QR ، وما إلى ذلك) |
| [BarcodeValue](../../aspose.words.fields/fielddisplaybarcode/barcodevalue/) { get; set; } | الحصول على قيمة الرمز الشريطي أو تعيينها. |
| [CaseCodeStyle](../../aspose.words.fields/fielddisplaybarcode/casecodestyle/) { get; set; } | الحصول على أو تحديد نمط رمز الحالة لنوع الرمز الشريطي ITF14. القيم الصالحة هي [STD &#x7C; EXT &#x7C; ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [DisplayText](../../aspose.words.fields/fielddisplaybarcode/displaytext/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم عرض بيانات الباركود (نص) مع الصورة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [ErrorCorrectionLevel](../../aspose.words.fields/fielddisplaybarcode/errorcorrectionlevel/) { get; set; } | الحصول على أو تعيين مستوى تصحيح الخطأ لرمز الاستجابة السريعة. القيم الصالحة هي [0 ، 3] . |
| [FixCheckDigit](../../aspose.words.fields/fielddisplaybarcode/fixcheckdigit/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إصلاح رقم التحقق إذا كان غير صالح. |
| [ForegroundColor](../../aspose.words.fields/fielddisplaybarcode/foregroundcolor/) { get; set; } | الحصول على أو تحديد اللون الأمامي لرمز الباركود. القيم الصالحة موجودة في النطاق [0 ، 0xFFFFFF] |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [PosCodeStyle](../../aspose.words.fields/fielddisplaybarcode/poscodestyle/) { get; set; } | الحصول على أو تعيين نمط الرمز الشريطي لنقطة البيع (أنواع الرموز الشريطية UPCA &#x7C; UPCE &#x7C; EAN13 &#x7C; EAN8). القيم الصالحة (غير حساسة لحالة الأحرف) هي [STD &#x7C; SUP2 &#x7C; SUP5 &#x7C; CASE] . |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [ScalingFactor](../../aspose.words.fields/fielddisplaybarcode/scalingfactor/) { get; set; } | الحصول على أو تعيين عامل تحجيم للرمز. القيمة بالنقاط المئوية الكاملة والقيم الصالحة هي [10 ، 1000] |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [SymbolHeight](../../aspose.words.fields/fielddisplaybarcode/symbolheight/) { get; set; } | الحصول على ارتفاع الرمز أو تحديده. الوحدات في TWIPS (1/1440 بوصة). |
| [SymbolRotation](../../aspose.words.fields/fielddisplaybarcode/symbolrotation/) { get; set; } | الحصول على أو تعيين تدوير رمز الباركود. القيم الصالحة هي [0 ، 3] |
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

إدراج رمز شريطي .

### أمثلة

يوضح كيفية إجراء دمج المراسلات على رموز QR الشريطية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل MERGEBARCODE ، والذي سيقبل القيم من مصدر البيانات أثناء دمج البريد.
// سيحول هذا الحقل جميع القيم الموجودة في عمود "MyQRCode" الخاص بمصدر بيانات الدمج إلى أكواد QR.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// تطبيق ألوان وقياسات مخصصة.
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyQRCode QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
    field.GetFieldCode());
builder.Writeln();

// قم بإنشاء DataTable بعمود بنفس الاسم مثل BarcodeValue الخاص بحقل MERGEBARCODE.
// سيقوم دمج البريد بإنشاء صفحة جديدة لكل صف. ستحتوي كل صفحة على حقل DISPLAYBARCODE ،
// الذي سيعرض رمز الاستجابة السريعة بالقيمة من الصف المدمج.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyQRCode");
table.Rows.Add(new[] { "ABC123" });
table.Rows.Add(new[] { "DEF456" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"ABC123\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B", 
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"DEF456\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.QR.docx");
```

يوضح كيفية إدراج حقل DISPLAYBARCODE وتعيين خصائصه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// يوجد أدناه أربعة أنواع من الرموز الشريطية ، مزينة بطرق مختلفة ، والتي يمكن أن يعرضها حقل DISPLAYBARCODE.
// 1 - رمز الاستجابة السريعة بألوان مخصصة:
field.BarcodeType = "QR";
field.BarcodeValue = "ABC123";
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field.GetFieldCode());
builder.Writeln();

// 2 - الباركود EAN13 ، مع عرض الأرقام أسفل الأشرطة:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - الرمز الشريطي CODE39:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - الباركود ITF4 ، مع رمز الحالة المحدد:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


