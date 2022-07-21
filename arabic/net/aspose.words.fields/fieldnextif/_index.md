---
title: FieldNextIf
second_title: Aspose.Words لمراجع .NET API
description: تنفيذ الحقل NEXTIF .
type: docs
weight: 2040
url: /ar/net/aspose.words.fields/fieldnextif/
---
## FieldNextIf class

تنفيذ الحقل NEXTIF .

```csharp
public class FieldNextIf : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldNextIf](fieldnextif)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldnextif/comparisonoperator) { get; set; } | الحصول على عامل المقارنة أو تعيينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format) { get; } | يحصل على أ[`FieldFormat`](../fieldformat) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LeftExpression](../../aspose.words.fields/fieldnextif/leftexpression) { get; set; } | الحصول على أو تعيين الجزء الأيسر من تعبير المقارنة. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [RightExpression](../../aspose.words.fields/fieldnextif/rightexpression) { get; set; } | الحصول على الجزء الصحيح من تعبير المقارنة أو تعيينه. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

مقارنة القيم المعينة بواسطة التعبيرات[`LeftExpression`](./leftexpression) و[`RightExpression`](./rightexpression) بالمقارنة باستخدام المشغل المعين من قبل[`ComparisonOperator`](./comparisonoperator) . إذا كانت المقارنة صحيحة ، يتم دمج سجل البيانات التالي في مستند الدمج الحالي. (يتم استبدال الحقول التي تتبع NEXTIF في المستند main بقيم من سجل البيانات التالي بدلاً من سجل البيانات الحالي.) إذا كانت المقارنة خاطئة ، يتم دمج سجل البيانات التالي في مستند دمج جديد.

### أمثلة

يوضح كيفية استخدام حقول NEXT / NEXTIF لدمج عدة صفوف في صفحة واحدة أثناء دمج المراسلات.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // إنشاء مصدر بيانات لدمج البريد الخاص بنا بثلاثة صفوف.
    // عادةً ما يؤدي دمج المراسلات الذي يستخدم هذا الجدول إلى إنشاء مستند من 3 صفحات.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // إذا كان لدينا عدة حقول دمج بنفس اسم الحقل ،
    // سيستقبلون البيانات من نفس الصف لمصدر البيانات ويعرضون نفس القيمة بعد الدمج.
    // يخبر الحقل التالي عملية دمج البريد على الفور بالتحرك لأسفل بمقدار صف واحد ،
    // مما يعني أن أي MERGEFIELDs التي تتبع الحقل التالي ستتلقى بيانات من الصف التالي.
    // تأكد من عدم محاولة التخطي إلى الصف التالي أثناء التواجد بالفعل في الصف الأخير.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // بعد الدمج ، قيم مصدر البيانات التي تقبلها MERGEFIELDs
     // ستنتهي في نفس الصفحة مثل MERGEFIELDs أعلاه.
    InsertMergeFields(builder, "Second row: ");

    // يحتوي حقل NEXTIF على نفس وظيفة الحقل التالي ،
    // لكنه ينتقل إلى الصف التالي فقط إذا كانت العبارة التي تم إنشاؤها بواسطة الخصائص الثلاثة التالية صحيحة.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // إذا كانت المقارنة التي أكدها الحقل أعلاه صحيحة ،
    // ستأخذ حقول الدمج الثلاثة التالية البيانات من الصف الثالث.
    // خلاف ذلك ، ستأخذ هذه الحقول البيانات من الصف 2 مرة أخرى.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // يحتوي مصدر البيانات لدينا على 3 صفوف ، وقد تخطينا الصفوف مرتين.
    // سيتضمن مستند الإخراج لدينا صفحة واحدة تحتوي على بيانات من جميع الصفوف الثلاثة.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");

/// <summary>
/// يستخدم منشئ المستندات لإدراج MERGEFIELDs لمصدر بيانات يحتوي على أعمدة باسم "Courtesy Title" و "First Name" و "Last Name".
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// يستخدم أداة إنشاء المستندات لإدراج MERRGEFIELD بخصائص محددة.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### أنظر أيضا

* class [Field](../field)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
