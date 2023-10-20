---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: Aspose.Words لـ .NET
description: MailMerge MergeWholeDocument ملكية. الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم تحديث الحقول الموجودة في المستند بأكمله أثناء تنفيذ دمج البريد مع المناطق في C#.
type: docs
weight: 70
url: /ar/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم تحديث الحقول الموجودة في المستند بأكمله أثناء تنفيذ دمج البريد مع المناطق.

```csharp
public bool MergeWholeDocument { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` .

## أمثلة

يُظهر العلاقة بين عمليات دمج البريد مع المناطق وتحديث الحقول.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // إذا قمنا بتعيين علامة "MergeWholeDocument" على "صحيح"،
    // سيؤدي دمج البريد مع المناطق إلى تحديث كل حقل في المستند.
    // إذا قمنا بتعيين علامة "MergeWholeDocument" على "خطأ"، فسيقوم دمج البريد بتحديث الحقول فقط
    // داخل منطقة دمج المراسلات التي يتطابق اسمها مع اسم جدول مصدر البيانات.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // سوف يقوم دمج المراسلات بتحديث حقل عرض الأسعار فقط خارج منطقة دمج المراسلات
    // إذا قمنا بتعيين علامة "MergeWholeDocument" على "صحيح".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// قم بإنشاء مستند بمنطقة دمج البريد التي تنتمي إلى مصدر بيانات يسمى "MyTable".
/// أدخل حقل اقتباس واحد داخل هذه المنطقة، وآخر خارجها.
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
/// قم بإنشاء جدول بيانات سيتم استخدامه في دمج البريد.
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
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
