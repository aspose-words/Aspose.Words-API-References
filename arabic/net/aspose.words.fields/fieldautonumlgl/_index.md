---
title: Class FieldAutoNumLgl
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldAutoNumLgl فصل. ينفذ الحقل AUTONUMLGL.
type: docs
weight: 1590
url: /ar/net/aspose.words.fields/fieldautonumlgl/
---
## FieldAutoNumLgl class

ينفذ الحقل AUTONUMLGL.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldAutoNumLgl : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldAutoNumLgl](fieldautonumlgl/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [RemoveTrailingPeriod](../../aspose.words.fields/fieldautonumlgl/removetrailingperiod/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم عرض الرقم بدون نقطة زائدة. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [SeparatorCharacter](../../aspose.words.fields/fieldautonumlgl/separatorcharacter/) { get; set; } | الحصول على أو تعيين الحرف الفاصل المطلوب استخدامه. |
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

إدراج رقم تلقائي بالتنسيق القانوني.

### أمثلة

يوضح كيفية تنظيم مستند باستخدام حقول AUTONUMLGL.

```csharp
public void FieldAutoNumLgl()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // تعرض حقول AUTONUMLGL رقمًا يتزايد في كل حقل AUTONUMLGL ضمن مستوى العنوان الحالي.
    // تحتفظ هذه الحقول بعدد منفصل لكل مستوى عنوان،
     // ويعرض كل حقل أيضًا أعداد حقول AUTONUMLGL لجميع مستويات العناوين الموجودة أسفل المستوى الخاص به.
    // يؤدي تغيير العدد لأي مستوى عنوان إلى إعادة تعيين الأعداد لجميع المستويات فوق هذا المستوى إلى 1.
    // هذا يسمح لنا بتنظيم وثيقتنا في شكل قائمة تفصيلية.
    // هذا هو أول حقل AUTONUMLGL عند مستوى العنوان 1، ويعرض "1." في الوثيقة.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // هذا هو الحقل AUTONUMLGL الثاني عند مستوى العنوان 1، لذلك سيعرض "2.".
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // هذا هو أول حقل AUTONUMLGL عند مستوى العنوان 2،
    // والعدد التلقائي لمستوى العنوان الموجود أسفله هو "2"، لذلك سيعرض "2.1."
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // هذا هو أول حقل AUTONUMLGL عند مستوى العنوان 3.
    // عند العمل بنفس طريقة الحقل أعلاه، سيتم عرض "2.1.1.".
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // هذا الحقل عند مستوى العنوان 2، وعدد AUTONUMLGL الخاص به عند 2، لذلك سيعرض الحقل "2.2.".
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // زيادة عدد AUTONUMLGL لمستوى عنوان أقل من هذا المستوى
    // قام بإعادة تعيين العدد لهذا المستوى بحيث يعرض هذا الحقل "2.2.1."
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal))
    {
        // الحرف الفاصل الذي يظهر في نتيجة الحقل مباشرة بعد الرقم،
        // هي نقطة التوقف بشكل افتراضي. إذا تركنا هذه الخاصية فارغة،
        // سيعرض حقلنا الأخير AUTONUMLGL "2.2.1." في الوثيقة.
        Assert.IsNull(field.SeparatorCharacter);

        // تعيين حرف فاصل مخصص وإزالة النقطة الزائدة
        // سيغير مظهر هذا الحقل من "2.2.1." إلى "2:2:1".
        // سوف نطبق هذا على كافة الحقول التي قمنا بإنشائها.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج عبارة مرقمة بواسطة حقل AUTONUMLGL.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // سينتمي هذا النص إلى الحقل القانوني للرقم التلقائي الموجود فوقه.
    // سوف ينهار عندما ننقر على السهم المجاور لحقل AUTONUMLGL المقابل في Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


