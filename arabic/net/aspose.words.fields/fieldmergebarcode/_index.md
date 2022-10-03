---
title: FieldMergeBarcode
second_title: Aspose.Words لمراجع .NET API
description: تنفيذ حقل MERGEBARCODE .
type: docs
weight: 1990
url: /ar/net/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class

تنفيذ حقل MERGEBARCODE .

```csharp
public class FieldMergeBarcode : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldMergeBarcode](fieldmergebarcode/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/fieldmergebarcode/addstartstopchar/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إضافة أحرف بدء / إيقاف لأنواع الباركود NW7 و CODE39. |
| [BackgroundColor](../../aspose.words.fields/fieldmergebarcode/backgroundcolor/) { get; set; } | الحصول على أو تحديد لون خلفية رمز الباركود. القيم الصالحة موجودة في النطاق [0 ، 0xFFFFFF] |
| [BarcodeType](../../aspose.words.fields/fieldmergebarcode/barcodetype/) { get; set; } | الحصول على نوع الرمز الشريطي أو تعيينه (QR ، وما إلى ذلك) |
| [BarcodeValue](../../aspose.words.fields/fieldmergebarcode/barcodevalue/) { get; set; } | الحصول على قيمة الرمز الشريطي أو تعيينها. |
| [CaseCodeStyle](../../aspose.words.fields/fieldmergebarcode/casecodestyle/) { get; set; } | الحصول على أو تحديد نمط رمز الحالة لنوع الرمز الشريطي ITF14. القيم الصالحة هي [STD &#x7C; EXT &#x7C; ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [DisplayText](../../aspose.words.fields/fieldmergebarcode/displaytext/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم عرض بيانات الباركود (نص) مع الصورة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [ErrorCorrectionLevel](../../aspose.words.fields/fieldmergebarcode/errorcorrectionlevel/) { get; set; } | الحصول على أو تعيين مستوى تصحيح الخطأ لرمز الاستجابة السريعة. القيم الصالحة هي [0 ، 3] . |
| [FixCheckDigit](../../aspose.words.fields/fieldmergebarcode/fixcheckdigit/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إصلاح رقم التحقق إذا كان غير صالح. |
| [ForegroundColor](../../aspose.words.fields/fieldmergebarcode/foregroundcolor/) { get; set; } | الحصول على أو تحديد اللون الأمامي لرمز الباركود. القيم الصالحة موجودة في النطاق [0 ، 0xFFFFFF] |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [PosCodeStyle](../../aspose.words.fields/fieldmergebarcode/poscodestyle/) { get; set; } | الحصول على أو تعيين نمط الرمز الشريطي لنقطة البيع (أنواع الرموز الشريطية UPCA &#x7C; UPCE &#x7C; EAN13 &#x7C; EAN8). القيم الصالحة (غير حساسة لحالة الأحرف) هي [STD &#x7C; SUP2 &#x7C; SUP5 &#x7C; CASE] . |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [ScalingFactor](../../aspose.words.fields/fieldmergebarcode/scalingfactor/) { get; set; } | الحصول على أو تعيين عامل تحجيم للرمز. القيمة بالنقاط المئوية الكاملة والقيم الصالحة هي [10 ، 1000] |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [SymbolHeight](../../aspose.words.fields/fieldmergebarcode/symbolheight/) { get; set; } | الحصول على ارتفاع الرمز أو تحديده. الوحدات في TWIPS (1/1440 بوصة). |
| [SymbolRotation](../../aspose.words.fields/fieldmergebarcode/symbolrotation/) { get; set; } | الحصول على أو تعيين تدوير رمز الباركود. القيم الصالحة هي [0 ، 3] |
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

دمج البريد في رمز شريطي .

### أمثلة

يوضح كيفية تنفيذ دمج المراسلات على الباركود ITF14.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل MERGEBARCODE ، والذي سيقبل القيم من مصدر البيانات أثناء دمج البريد.
// سيحول هذا الحقل جميع القيم الموجودة في عمود "MyITF14Barcode" الخاص بمصدر بيانات الدمج إلى رموز شريطية لـ ITF14.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// قم بإنشاء DataTable بعمود بنفس الاسم مثل BarcodeValue الخاص بحقل MERGEBARCODE.
// سيقوم دمج البريد بإنشاء صفحة جديدة لكل صف. ستحتوي كل صفحة على حقل DISPLAYBARCODE ،
// الذي سيعرض الرمز الشريطي ITF14 بالقيمة من الصف المدمج.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyITF14Barcode");
table.Rows.Add(new[] { "09312345678907" });
table.Rows.Add(new[] { "1234567891234" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"09312345678907\" ITF14 \\c STD",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"1234567891234\" ITF14 \\c STD",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.ITF14.docx");
```

يوضح كيفية تنفيذ دمج المراسلات على الرموز الشريطية CODE39.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل MERGEBARCODE ، والذي سيقبل القيم من مصدر البيانات أثناء دمج البريد.
// سيقوم هذا الحقل بتحويل جميع القيم الموجودة في عمود "MyCODE39Barcode" الخاص بمصدر بيانات الدمج إلى الرموز الشريطية CODE39.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// تحرير مظهره لعرض أحرف البداية / الإيقاف.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// قم بإنشاء DataTable بعمود بنفس الاسم مثل BarcodeValue الخاص بحقل MERGEBARCODE.
// سيقوم دمج البريد بإنشاء صفحة جديدة لكل صف. ستحتوي كل صفحة على حقل DISPLAYBARCODE ،
// الذي سيعرض الرمز الشريطي CODE39 بالقيمة من الصف المدمج.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyCODE39Barcode");
table.Rows.Add(new[] { "12345ABCDE" });
table.Rows.Add(new[] { "67890FGHIJ" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"12345ABCDE\" CODE39 \\d",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"67890FGHIJ\" CODE39 \\d",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.CODE39.docx");
```

يوضح كيفية تنفيذ دمج البريد على الرموز الشريطية EAN13.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل MERGEBARCODE ، والذي سيقبل القيم من مصدر البيانات أثناء دمج البريد.
// سيحول هذا الحقل جميع القيم الموجودة في عمود "MyEAN13Barcode" الخاص بمصدر بيانات الدمج إلى رموز شريطية لـ EAN13.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// عرض القيمة الرقمية للرمز الشريطي أسفل الأشرطة.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// قم بإنشاء DataTable بعمود بنفس الاسم مثل BarcodeValue الخاص بحقل MERGEBARCODE.
// سيقوم دمج البريد بإنشاء صفحة جديدة لكل صف. ستحتوي كل صفحة على حقل DISPLAYBARCODE ،
// الذي سيعرض الرمز الشريطي EAN13 بالقيمة من الصف المدمج.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyEAN13Barcode");
table.Rows.Add(new[] { "501234567890" });
table.Rows.Add(new[] { "123456789012" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"501234567890\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"123456789012\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.EAN13.docx");
```

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

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
