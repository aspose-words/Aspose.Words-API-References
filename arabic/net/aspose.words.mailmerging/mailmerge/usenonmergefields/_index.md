---
title: MailMerge.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words لـ .NET
description: MailMerge UseNonMergeFields ملكية. متىحقيقي  يحدد أنه بالإضافة إلى حقول MERGEFIELD يتم إجراء دمج البريد في بعض أنواع الحقول الأخرى و أيضًا في علامات fieldName في C#.
type: docs
weight: 150
url: /ar/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

متى`حقيقي` ، يحدد أنه بالإضافة إلى حقول MERGEFIELD، يتم إجراء دمج البريد في بعض أنواع الحقول الأخرى و أيضًا في علامات "{{fieldName}}".

```csharp
public bool UseNonMergeFields { get; set; }
```

## ملاحظات

عادةً، يتم تنفيذ دمج البريد فقط في حقول MERGEFIELD، ولكن تم إنشاء التقارير الخاصة بالعديد من العملاء باستخدام حقول أخرى وتم إنشاء العديد من المستندات بهذه الطريقة. لتبسيط الترحيل (ولأن أسلوب هذا تم استخدامه بشكل مستقل من قبل العديد من العملاء) تم تقديم القدرة على دمج البريد في الحقول الأخرى.

متى`UseNonMergeFields` تم ضبطه على`حقيقي`، سيقوم Aspose.Words بدمج البريد في الحقول التالية:

اسم حقل ميرجيفيلد

MACROBUTTON NOMACRO اسم الحقل

إذا 0 = 0 "{FieldName}" ""

وأيضا متى`UseNonMergeFields` تم ضبطه على`حقيقي`، سيقوم Aspose.Words بدمج البريد في العلامات النصية "{{fieldName}}". هذه ليست حقول، ولكنها مجرد علامات نصية.

## أمثلة

يوضح كيفية الحفاظ على مظهر علامات دمج البريد البديلة التي لا يتم استخدامها أثناء عملية دمج البريد.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // بشكل افتراضي، يقوم دمج البريد بوضع البيانات من كل صف من الجدول في MERGEFIELDs، والتي تسمي الأعمدة في هذا الجدول.
    // لا تحتوي وثيقتنا على مثل هذه الحقول، ولكنها تحتوي على علامات نص عادي محاطة بأقواس متعرجة.
    // إذا قمنا بتعيين علامة "PreserveUnusedTags" على "true"، فيمكننا التعامل مع هذه العلامات على أنها MERGEFIELDs
    // للسماح لدمج البريد الخاص بنا بإدراج البيانات من مصدر البيانات في تلك العلامات.
    // إذا قمنا بتعيين علامة "PreserveUnusedTags" على "خطأ"،
    // سيؤدي دمج البريد إلى تحويل هذه العلامات إلى علامات MERGEFIELD وتركها شاغرة.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // تحتوي وثيقتنا على علامة لعمود يسمى "Column2"، وهو غير موجود في الجدول.
    // إذا قمنا بتعيين علامة "PreserveUnusedTags" على "خطأ"، then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// أنشئ مستندًا وأضف علامتي نص عادي قد تعملان كـ MERGEFIELDs أثناء دمج البريد.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // سيتم تسجيل علاماتنا كوجهات لبيانات دمج البريد فقط إذا قمنا بتعيين هذا على "صحيح".
    doc.MailMerge.UseNonMergeFields = true;

    return doc;
}

/// <summary>
/// أنشئ جدول بيانات بسيطًا بعمود واحد.
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
