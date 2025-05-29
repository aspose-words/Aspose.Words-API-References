---
title: MailMerge.MergeDuplicateRegions
linktitle: MergeDuplicateRegions
articleTitle: MergeDuplicateRegions
second_title: Aspose.Words لـ .NET
description: حسّن عملية دمج البريد باستخدام خاصية MergeDuplicateRegions. تحكّم في كيفية دمج مناطق مصدر البيانات لإدارة مستندات فعّالة.
type: docs
weight: 60
url: /ar/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

يحصل على قيمة أو يعينها تشير إلى ما إذا كان يجب دمج جميع مناطق دمج البريد للمستندات التي تحمل اسم مصدر البيانات أثناء تنفيذ دمج البريد مع المناطق مقابل مصدر البيانات أو المنطقة الأولى فقط.

```csharp
public bool MergeDuplicateRegions { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` .

## أمثلة

يوضح كيفية العمل مع مناطق دمج البريد المكررة.

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // إذا قمنا بتعيين خاصية "MergeDuplicateRegions" إلى "false"، فسوف يؤثر دمج البريد على المنطقة الأولى،
    // بينما سيتم ترك MERGEFIELDs للثاني في حالة ما قبل الدمج.
    // للحصول على كلا المنطقتين مدمجتين بهذه الطريقة،
    // سيتعين علينا تنفيذ دمج البريد مرتين على جدول يحمل نفس الاسم.
    // إذا قمنا بتعيين خاصية "MergeDuplicateRegions" إلى "true"، فسوف يؤثر دمج البريد على كلا المنطقتين.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// إرجاع مستند يحتوي على منطقتين مكررتين لدمج البريد (تشتركان في نفس الاسم في علامتي "TableStart/End").
/// </summary>
private static Document CreateSourceDocMergeDuplicateRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column1");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");

    return doc;
}

/// <summary>
/// إنشاء جدول بيانات يحتوي على صف واحد وعمودين.
/// </summary>
private static DataTable CreateSourceTableMergeDuplicateRegions()
{
    DataTable dataTable = new DataTable("MergeRegion");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
