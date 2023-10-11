---
title: FieldAutoNumLgl.RemoveTrailingPeriod
second_title: Aspose.Words لمراجع .NET API
description: FieldAutoNumLgl ملكية. الحصول على أو تعيين ما إذا كان سيتم عرض الرقم بدون نقطة زائدة.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldautonumlgl/removetrailingperiod/
---
## FieldAutoNumLgl.RemoveTrailingPeriod property

الحصول على أو تعيين ما إذا كان سيتم عرض الرقم بدون نقطة زائدة.

```csharp
public bool RemoveTrailingPeriod { get; set; }
```

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

* class [FieldAutoNumLgl](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldautonumlgl/)
* المجسم [Aspose.Words](../../../)


