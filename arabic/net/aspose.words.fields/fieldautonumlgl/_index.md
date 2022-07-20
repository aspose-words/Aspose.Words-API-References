---
title: FieldAutoNumLgl
second_title: Aspose.Words لمراجع .NET API
description: تنفذ حقل AUTONUMLGL .
type: docs
weight: 1440
url: /ar/net/aspose.words.fields/fieldautonumlgl/
---
## FieldAutoNumLgl class

تنفذ حقل AUTONUMLGL .

```csharp
public class FieldAutoNumLgl : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldAutoNumLgl](fieldautonumlgl)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format) { get; } | يحصل على أ[`FieldFormat`](../fieldformat) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [RemoveTrailingPeriod](../../aspose.words.fields/fieldautonumlgl/removetrailingperiod) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم عرض الرقم بدون نقطة لاحقة. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [SeparatorCharacter](../../aspose.words.fields/fieldautonumlgl/separatorcharacter) { get; set; } | الحصول على أو تعيين الحرف الفاصل الذي سيتم استخدامه. |
| [Start](../../aspose.words.fields/field/start) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) ._ x000d_ يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) ._ x000d_ |
| [Remove](../../aspose.words.fields/field/remove)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

يتم إدخال رقم تلقائي بتنسيق قانوني .

### أمثلة

يوضح كيفية تنظيم مستند باستخدام حقول AUTONUMLGL.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // تعرض حقول AUTONUMLGL رقمًا يتزايد في كل حقل AUTONUMLGL ضمن مستوى العنوان الحالي.
    // تحتفظ هذه الحقول بعدد منفصل لكل مستوى عنوان ،
     // ويعرض كل حقل أيضًا عدد حقول AUTONUMLGL لجميع مستويات العناوين الموجودة أسفل مستوى الحقل الخاص به.
    // يؤدي تغيير العد لأي مستوى عنوان إلى إعادة تعيين التهم لجميع المستويات فوق هذا المستوى إلى 1.
    // هذا يسمح لنا بتنظيم وثيقتنا في شكل قائمة مخطط تفصيلي.
    // هذا هو أول حقل AUTONUMLGL بمستوى عنوان 1 ، ويعرض "1." في المستند.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // هذا هو حقل AUTONUMLGL الثاني عند مستوى عنوان 1 ، لذلك سيعرض "2.".
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // هذا هو أول حقل AUTONUMLGL بمستوى عنوان 2 ،
    // وعدد AUTONUMLGL لمستوى العنوان أدناه هو "2" ، لذلك سيعرض "2.1.".
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // هذا هو أول حقل AUTONUMLGL بمستوى عنوان 3.
    // يعمل بنفس طريقة الحقل أعلاه ، سيعرض "2.1.1.".
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // هذا الحقل في مستوى عنوان 2 ، وعدد AUTONUMLGL الخاص به هو 2 ، لذلك سيعرض الحقل "2.2.".
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // زيادة عدد AUTONUMLGL لمستوى عنوان أقل من هذا المستوى
    // أعاد تعيين العد لهذا المستوى بحيث يعرض هذا الحقل "2.2.1.".
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal))
    {
        // الحرف الفاصل الذي يظهر في نتيجة الحقل مباشرة بعد الرقم ،
        // هي نقطة توقف كاملة بشكل افتراضي. إذا تركنا هذه الخاصية فارغة ،
        // سيعرض حقل AUTONUMLGL الأخير "2.2.1." في المستند.
        Assert.IsNull(field.SeparatorCharacter);

        // تعيين حرف فاصل مخصص وإزالة الفترة اللاحقة
        // سيغير مظهر هذا الحقل من "2.2.1." إلى "2: 2: 1".
        // سنطبق هذا على جميع الحقول التي أنشأناها.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");

/// <summary>
/// يستخدم أداة إنشاء المستندات لإدراج بند مرقم بواسطة حقل AUTONUMLGL.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // سينتمي هذا النص إلى حقل العدد القانوني التلقائي فوقه.
    // سينهار عندما نضغط على السهم بجوار حقل AUTONUMLGL المقابل في Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### أنظر أيضا

* class [Field](../field)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
