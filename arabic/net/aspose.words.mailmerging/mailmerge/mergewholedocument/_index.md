---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم خاصية MailMerge MergeWholeDocument بتحديث جميع الحقول أثناء دمج البريد المستند إلى المنطقة، مما يعزز الكفاءة والدقة في مستنداتك.
type: docs
weight: 70
url: /ar/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت الحقول في المستند بأكمله يتم تحديثها أثناء تنفيذ دمج البريد مع المناطق.

```csharp
public bool MergeWholeDocument { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` .

## أمثلة

يُظهر العلاقة بين دمج البريد مع المناطق وتحديث الحقل.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // إذا قمنا بتعيين علامة "MergeWholeDocument" إلى "true"،
    // سيؤدي دمج البريد مع المناطق إلى تحديث كل حقل في المستند.
    // إذا قمنا بتعيين علامة "MergeWholeDocument" إلى "false"، فسوف يقوم دمج البريد بتحديث الحقول فقط
    // ضمن منطقة دمج البريد التي يتطابق اسمها مع اسم جدول مصدر البيانات.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // سوف يقوم دمج البريد بتحديث حقل الاقتباس خارج منطقة دمج البريد فقط
    // إذا قمنا بتعيين العلم "MergeWholeDocument" إلى "true".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// قم بإنشاء مستند بمنطقة دمج بريد تنتمي إلى مصدر بيانات يسمى "MyTable".
/// أدخل حقل اقتباس واحد داخل هذه المنطقة، وحقل آخر خارجها.
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
