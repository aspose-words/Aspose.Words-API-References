---
title: MailMerge.PreserveUnusedTags
second_title: Aspose.Words لمراجع .NET API
description: MailMerge ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كان يجب الاحتفاظ بعلامات الشارب غير المستخدمة.
type: docs
weight: 80
url: /ar/net/aspose.words.mailmerging/mailmerge/preserveunusedtags/
---
## MailMerge.PreserveUnusedTags property

الحصول على أو تعيين قيمة تشير إلى ما إذا كان يجب الاحتفاظ بعلامات "الشارب" غير المستخدمة.

```csharp
public bool PreserveUnusedTags { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`خطأ شنيع` .

### أمثلة

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

* property [UseNonMergeFields](../usenonmergefields/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)


