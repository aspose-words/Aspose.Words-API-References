---
title: FieldAutoNumLgl.RemoveTrailingPeriod
linktitle: RemoveTrailingPeriod
articleTitle: RemoveTrailingPeriod
second_title: Aspose.Words لـ .NET
description: قم بإدارة خاصية RemoveTrailingPeriod في FieldAutoNumLgl لتخصيص عرض الأرقام - قم بإزالة النقاط الزائدة للحصول على تنسيق أكثر نظافة واحترافية.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldautonumlgl/removetrailingperiod/
---
## FieldAutoNumLgl.RemoveTrailingPeriod property

يحصل على أو يحدد ما إذا كان سيتم عرض الرقم بدون نقطة نهاية.

```csharp
public bool RemoveTrailingPeriod { get; set; }
```

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

* class [FieldAutoNumLgl](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
