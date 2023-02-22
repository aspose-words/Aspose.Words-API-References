---
title: MailMerge.MergeWholeDocument
second_title: Aspose.Words لمراجع .NET API
description: MailMerge ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم تحديث الحقول في المستند بأكمله أثناء تنفيذ دمج البريد مع المناطق.
type: docs
weight: 70
url: /ar/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم تحديث الحقول في المستند بأكمله أثناء تنفيذ دمج البريد مع المناطق.

```csharp
public bool MergeWholeDocument { get; set; }
```

### ملاحظات

القيمة الافتراضية هي **خاطئة** .

### أمثلة

إظهار العلاقة بين دمج البريد مع المناطق وتحديث الحقل.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // إذا قمنا بتعيين علامة "MergeWholeDocument" على "true" ،
    // سيؤدي دمج البريد مع المناطق إلى تحديث كل حقل في المستند.
    // إذا قمنا بتعيين علامة "MergeWholeDocument" على "خطأ" ، فلن يقوم دمج البريد إلا بتحديث الحقول
    // داخل منطقة دمج المراسلات التي يتطابق اسمها مع اسم جدول مصدر البيانات.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // لن يقوم دمج المراسلات إلا بتحديث حقل QUOTE خارج منطقة دمج المراسلات
    // إذا قمنا بتعيين علامة "MergeWholeDocument" على "true".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// إنشاء مستند بمنطقة دمج المراسلات التي تنتمي إلى مصدر بيانات يسمى "MyTable".
/// أدخل حقل اقتباس واحد داخل هذه المنطقة وآخر خارجها.
/// </summary>
private static Document CreateSourceDocMergeWholeDocument()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is outside of the \"MyTable\" merge region.";

    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD TableStart:MyTable");

    field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is inside the \"MyTable\" merge region.";
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD MyColumn");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    return doc;
}

/// <summary>
/// إنشاء جدول البيانات الذي سيتم استخدامه في دمج البريد.
/// </summary>
private static DataTable CreateSourceTableMergeWholeDocument()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("MyColumn");
    dataTable.Rows.Add(new object[] { "MyValue" });

    return dataTable;
}
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)


