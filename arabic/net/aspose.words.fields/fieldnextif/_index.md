---
title: FieldNextIf Class
linktitle: FieldNextIf
articleTitle: FieldNextIf
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.FieldNextIf فصل. ينفذ الحقل NEXTIF في C#.
type: docs
weight: 2190
url: /ar/net/aspose.words.fields/fieldnextif/
---
## FieldNextIf class

ينفذ الحقل NEXTIF.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldNextIf : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldNextIf](fieldnextif/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldnextif/comparisonoperator/) { get; set; } | الحصول على عامل المقارنة أو تعيينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LeftExpression](../../aspose.words.fields/fieldnextif/leftexpression/) { get; set; } | الحصول على أو تعيين الجزء الأيسر من تعبير المقارنة. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [RightExpression](../../aspose.words.fields/fieldnextif/rightexpression/) { get; set; } | الحصول على أو تعيين الجزء الأيمن من تعبير المقارنة. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

## ملاحظات

يقارن القيم المعينة بالتعبيرات[`LeftExpression`](./leftexpression/) و[`RightExpression`](./rightexpression/) بالمقارنة باستخدام عامل التشغيل المعين بواسطة[`ComparisonOperator`](./comparisonoperator/) . إذا كانت المقارنة صحيحة، فسيتم دمج سجل البيانات التالي في مستند الدمج الحالي. (يتم استبدال حقول الدمج التي تتبع NEXTIF في المستند main بقيم من سجل البيانات التالي بدلاً من سجل البيانات الحالي.) إذا كانت المقارنة خاطئة، فسيتم دمج سجل البيانات التالي في مستند دمج جديد.

## أمثلة

يوضح كيفية استخدام حقول NEXT/NEXTIF لدمج صفوف متعددة في صفحة واحدة أثناء عملية دمج البريد.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أنشئ مصدر بيانات لدمج البريد لدينا بثلاثة صفوف.
    // عادةً ما يؤدي دمج البريد الذي يستخدم هذا الجدول إلى إنشاء مستند من 3 صفحات.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // إذا كان لدينا حقول دمج متعددة بنفس اسم الحقل،
    // سوف يتلقون البيانات من نفس الصف من مصدر البيانات ويعرضون نفس القيمة بعد الدمج.
    // يخبر الحقل التالي دمج المراسلات على الفور بالتحرك لأسفل صفًا واحدًا،
    // مما يعني أن أي MERGEFIELDs تتبع الحقل التالي ستتلقى بيانات من الصف التالي.
    // تأكد من عدم محاولة الانتقال إلى الصف التالي مطلقًا أثناء وجودك في الصف الأخير.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // بعد الدمج، قيم مصدر البيانات التي تقبلها وحدات MERGEFIELD هذه
     // سينتهي في نفس الصفحة مثل MERGEFIELDs أعلاه.
    InsertMergeFields(builder, "Second row: ");

    // الحقل NEXTIF له نفس وظيفة الحقل التالي،
    // ولكنه ينتقل إلى الصف التالي فقط إذا كانت العبارة التي تم إنشاؤها بواسطة الخصائص الثلاث التالية صحيحة.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // إذا كانت المقارنة التي يؤكدها الحقل أعلاه صحيحة،
    // ستأخذ حقول الدمج الثلاثة التالية البيانات من الصف الثالث.
    // بخلاف ذلك، ستأخذ هذه الحقول البيانات من الصف 2 مرة أخرى.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // يحتوي مصدر البيانات لدينا على 3 صفوف، وقمنا بتخطي الصفوف مرتين.
    // سيحتوي مستند الإخراج الخاص بنا على صفحة واحدة تحتوي على بيانات من جميع الصفوف الثلاثة.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج MERGEFIELDs لمصدر بيانات يحتوي على أعمدة تسمى "عنوان الخدمة" و"الاسم الأول" و"اسم العائلة".
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج MERRGEFIELD بخصائص محددة.
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

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
