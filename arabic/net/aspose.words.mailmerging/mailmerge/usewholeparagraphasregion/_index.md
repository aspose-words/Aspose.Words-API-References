---
title: MailMerge.UseWholeParagraphAsRegion
second_title: Aspose.Words لمراجع .NET API
description: MailMerge ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كان يجب تضمين فقرة كاملة مع TableStart أو TableEnd field أو نطاق معين بين حقول TableStart و TableEnd في منطقة دمج المراسلات.
type: docs
weight: 160
url: /ar/net/aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/
---
## MailMerge.UseWholeParagraphAsRegion property

الحصول على أو تعيين قيمة تشير إلى ما إذا كان يجب تضمين فقرة كاملة مع TableStart أو TableEnd field أو نطاق معين بين حقول TableStart و TableEnd في منطقة دمج المراسلات.

```csharp
public bool UseWholeParagraphAsRegion { get; set; }
```

### ملاحظات

القيمة الافتراضية هي **حقيقي** .

### أمثلة

إظهار العلاقة بين مناطق دمج المراسلات والفقرات.

```csharp
public void UseWholeParagraphAsRegion(bool useWholeParagraphAsRegion)
{
    Document doc = CreateSourceDocWithNestedMergeRegions();
    DataTable dataTable = CreateSourceTableDataTableForOneRegion();

    // بشكل افتراضي ، لا يمكن أن تنتمي فقرة إلى أكثر من منطقة واحدة لدمج المراسلات.
    // محتويات وثيقتنا لا تفي بهذه المعايير.
    // إذا قمنا بتعيين علامة "UseWholeParagraphAsRegion" على "true" ،
    // سيؤدي تشغيل دمج المراسلات في هذا المستند إلى طرح استثناء.
    // إذا قمنا بتعيين علامة "UseWholeParagraphAsRegion" على "false" ،
    // سنتمكن من تنفيذ دمج المراسلات في هذا المستند.
    doc.MailMerge.UseWholeParagraphAsRegion = useWholeParagraphAsRegion;

    if (useWholeParagraphAsRegion)
        Assert.Throws<InvalidOperationException>(() => doc.MailMerge.ExecuteWithRegions(dataTable));
    else
        doc.MailMerge.ExecuteWithRegions(dataTable);

    // يملأ دمج المراسلات منطقتنا الأولى مع ترك المنطقة الثانية غير مستخدمة
    // لأنها المنطقة التي تخرق القاعدة.
    doc.Save(ArtifactsDir + "MailMerge.UseWholeParagraphAsRegion.docx");
}

/// <summary>
/// إنشاء مستند مع منطقتين لدمج المراسلات تشتركان في فقرة واحدة.
/// </summary>
private static Document CreateSourceDocWithNestedMergeRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Region 1: ");
    builder.InsertField(" MERGEFIELD TableStart:MyTable");
    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    builder.Write(", Region 2: ");
    builder.InsertField(" MERGEFIELD TableStart:MyOtherTable");
    builder.InsertField(" MERGEFIELD TableEnd:MyOtherTable");

    return doc;
}

/// <summary>
/// إنشاء جدول بيانات يمكنه ملء منطقة واحدة أثناء دمج البريد.
/// </summary>
private static DataTable CreateSourceTableDataTableForOneRegion()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)


