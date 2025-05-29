---
title: FieldAutoNumLgl Class
linktitle: FieldAutoNumLgl
articleTitle: FieldAutoNumLgl
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldAutoNumLgl للتنفيذ السلس لحقول AUTONUMLGL، وتحسين أتمتة المستندات وتنسيقها.
type: docs
weight: 2000
url: /ar/net/aspose.words.fields/fieldautonumlgl/
---
## FieldAutoNumLgl class

ينفذ حقل AUTONUMLGL.

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
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [RemoveTrailingPeriod](../../aspose.words.fields/fieldautonumlgl/removetrailingperiod/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم عرض الرقم بدون نقطة نهاية. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [SeparatorCharacter](../../aspose.words.fields/fieldautonumlgl/separatorcharacter/) { get; set; } | يحصل على حرف الفاصل الذي سيتم استخدامه أو يعينه. |
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

يُدرج رقمًا تلقائيًا بتنسيق قانوني.

## أمثلة

يوضح كيفية تنظيم مستند باستخدام حقول AUTONUMLGL.

```csharp
public void FieldAutoNumLgl()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // تعرض حقول AUTONUMLGL رقمًا يتزايد عند كل حقل AUTONUMLGL ضمن مستوى عنوانه الحالي.
    // تحتفظ هذه الحقول بعدد منفصل لكل مستوى عنوان،
     // ويعرض كل حقل أيضًا عدد حقول AUTONUMLGL لجميع مستويات العناوين أسفل مستواه الخاص.
    // يؤدي تغيير العدد لأي مستوى عنوان إلى إعادة تعيين العدد لجميع المستويات أعلى هذا المستوى إلى 1.
    // وهذا يسمح لنا بتنظيم مستندنا في شكل قائمة مخططة.
    // هذا هو أول حقل AUTONUMLGL على مستوى العنوان 1، ويعرض "1." في المستند.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // هذا هو حقل AUTONUMLGL الثاني على مستوى العنوان 1، لذلك سيعرض "2".
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // هذا هو أول حقل AUTONUMLGL على مستوى العنوان 2،
    // وعدد AUTONUMLGL لمستوى العنوان أدناه هو "2"، لذلك سيتم عرض "2.1".
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // هذا هو أول حقل AUTONUMLGL في مستوى العنوان 3.
    // العمل بنفس طريقة الحقل أعلاه، وسوف يعرض "2.1.1".
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // يقع هذا الحقل عند مستوى العنوان 2، ويبلغ عدد AUTONUMLGL الخاص به 2، لذا سيعرض الحقل "2.2".
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // زيادة عدد AUTONUMLGL لمستوى عنوان أقل من هذا المستوى
    // تم إعادة تعيين العدد لهذا المستوى بحيث يعرض هذا الحقل "2.2.1".
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal).ToList())
    {
        // حرف الفاصل الذي يظهر في حقل النتيجة مباشرة بعد الرقم،
        // هي نقطة افتراضيًا. إذا تركنا هذه الخاصية فارغة،
        // سيعرض حقل AUTONUMLGL الأخير لدينا "2.2.1." في المستند.
        Assert.IsNull(field.SeparatorCharacter);

        // تعيين حرف فاصل مخصص وإزالة النقطة النهائية
        //سيتم تغيير مظهر هذا الحقل من "2.2.1." إلى "2:2:1".
        //سنطبق هذا على جميع الحقول التي أنشأناها.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج شرط مرقم بواسطة حقل AUTONUMLGL.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // هذا النص سوف ينتمي إلى حقل الرقم القانوني التلقائي الموجود أعلىه.
    // سوف ينهار عندما نضغط على السهم الموجود بجوار الحقل AUTONUMLGL المقابل في Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
