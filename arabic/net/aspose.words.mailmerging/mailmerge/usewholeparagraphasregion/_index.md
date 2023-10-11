---
title: MailMerge.UseWholeParagraphAsRegion
second_title: Aspose.Words لمراجع .NET API
description: MailMerge ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كانت الفقرة بأكملها بها TableStart أو نهاية الجدول field أو نطاق معين بين TableStart و نهاية الجدول يجب تضمين الحقول في منطقة دمج البريد.
type: docs
weight: 160
url: /ar/net/aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/
---
## MailMerge.UseWholeParagraphAsRegion property

الحصول على أو تعيين قيمة تشير إلى ما إذا كانت الفقرة بأكملها بها **TableStart** أو **نهاية الجدول** field أو نطاق معين بين **TableStart** و **نهاية الجدول** يجب تضمين الحقول في منطقة دمج البريد.

```csharp
public bool UseWholeParagraphAsRegion { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`حقيقي` .

### أمثلة

إظهار العلاقة بين مناطق دمج البريد والفقرات.

```csharp
public void UseWholeParagraphAsRegion(bool useWholeParagraphAsRegion)
{
    Document doc = CreateSourceDocWithNestedMergeRegions();
    DataTable dataTable = CreateSourceTableDataTableForOneRegion();

    // بشكل افتراضي، لا يمكن أن تنتمي الفقرة إلى أكثر من منطقة واحدة لدمج البريد.
    // محتويات وثيقتنا لا تفي بهذه المعايير.
    // إذا قمنا بتعيين علامة "UseWholeParagraphAsRegion" على "صحيح"،
    // سيؤدي تشغيل دمج البريد في هذا المستند إلى حدوث استثناء.
    // إذا قمنا بتعيين علامة "UseWholeParagraphAsRegion" على "خطأ"،
    // سنكون قادرين على تنفيذ دمج البريد في هذا المستند.
    doc.MailMerge.UseWholeParagraphAsRegion = useWholeParagraphAsRegion;

    if (useWholeParagraphAsRegion)
        Assert.Throws<InvalidOperationException>(() => doc.MailMerge.ExecuteWithRegions(dataTable));
    else
        doc.MailMerge.ExecuteWithRegions(dataTable);

    // يملأ دمج المراسلات منطقتنا الأولى مع ترك المنطقة الثانية غير مستخدمة
    // بما أن المنطقة هي التي تكسر القاعدة.
    doc.Save(ArtifactsDir + "MailMerge.UseWholeParagraphAsRegion.docx");
}

/// <summary>
/// قم بإنشاء مستند يحتوي على منطقتين لدمج البريد تتشاركان في فقرة واحدة.
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
/// قم بإنشاء جدول بيانات يمكنه ملء منطقة واحدة أثناء دمج البريد.
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


