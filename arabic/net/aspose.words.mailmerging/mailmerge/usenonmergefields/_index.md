---
title: MailMerge.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words لـ .NET
description: أطلق العنان لقوة دمج البريد! استخدم خاصية UseNonMergeFields لتحسين مستنداتك عبر دمج أنواع الحقول المختلفة بسلاسة.
type: docs
weight: 150
url: /ar/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

عندما`حقيقي` , يحدد أنه بالإضافة إلى حقول MERGEFIELD، يتم تنفيذ دمج البريد في بعض الأنواع الأخرى من الحقول و أيضًا في علامات "{{fieldName}}".

```csharp
public bool UseNonMergeFields { get; set; }
```

## ملاحظات

عادةً، يُنفَّذ دمج البريد في حقول MERGEFIELD فقط، ولكن العديد من العملاء بنوا ملف reporting الخاص بهم باستخدام حقول أخرى، وأنشأوا العديد من المستندات بهذه الطريقة. لتبسيط عملية الترحيل (ولأن العديد من العملاء استخدموا هذا النهج بشكل مستقل)، أُضيفت إمكانية دمج البريد في حقول أخرى.

متى`UseNonMergeFields` تم ضبطه على`حقيقي`سيقوم Aspose.Words بتنفيذ عملية دمج البريد في الحقول التالية:

اسم حقل MERGEFIELD

MACROBUTTON NOMACRO اسم الحقل

إذا 0 = 0 "{اسم الحقل}" ""

أيضا، عندما`UseNonMergeFields` تم ضبطه على`حقيقي`سيقوم Aspose.Words بدمج البريد في علامات النص tags "{{fieldName}}". هذه ليست حقولاً، بل مجرد علامات نصية.

## أمثلة

يوضح كيفية الحفاظ على مظهر علامات دمج البريد البديلة التي لا يتم استخدامها أثناء دمج البريد.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // بشكل افتراضي، يقوم دمج البريد بوضع البيانات من كل صف من الجدول في MERGEFIELDs، والتي تقوم بتسمية الأعمدة في هذا الجدول.
    // لا تحتوي مستندنا على مثل هذه الحقول، ولكنها تحتوي على علامات نصية عادية محاطة بأقواس متعرجة.
    // إذا قمنا بتعيين علامة "PreserveUnusedTags" إلى "true"، فيمكننا التعامل مع هذه العلامات كـ MERGEFIELDs
    // للسماح لدمج البريد الخاص بنا بإدراج البيانات من مصدر البيانات في تلك العلامات.
    // إذا قمنا بتعيين علامة "PreserveUnusedTags" إلى "false"،
    // سيؤدي دمج البريد إلى تحويل هذه العلامات إلى MERGEFIELDs وتركها غير مملوءة.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // تحتوي مستندنا على علامة لعمود يسمى "Column2"، وهو غير موجود في الجدول.
    // إذا قمنا بتعيين علامة "PreserveUnusedTags" إلى "false"، then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// قم بإنشاء مستند وأضف علامتي نص عاديتين يمكنهما العمل كحقول MERGEFIELD أثناء دمج البريد.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // سيتم تسجيل علاماتنا كوجهات لبيانات دمج البريد فقط إذا قمنا بتعيين هذا على true.
    doc.MailMerge.UseNonMergeFields = true;

    return doc;
}

/// <summary>
/// قم بإنشاء جدول بيانات بسيط بعمود واحد.
/// </summary>
private static DataTable CreateSourceTablePreserveUnusedTags()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Rows.Add(new object[] { "Value1" });

    return dataTable;
}
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
