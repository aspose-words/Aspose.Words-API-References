---
title: Document.MailMerge
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. إرجاع أ دمج المراسلات كائن يمثل وظيفة دمج المراسلات للمستند.
type: docs
weight: 240
url: /ar/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

إرجاع أ **دمج المراسلات** كائن يمثل وظيفة دمج المراسلات للمستند.

```csharp
public MailMerge MailMerge { get; }
```

### أمثلة

يوضح كيفية تنفيذ دمج البريد مع البيانات من DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // فيما يلي طريقتان لاستخدام DataTable كمصدر بيانات لدمج البريد.
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريد ناتج واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند دمج بريد ناتج واحد:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// ينشئ مستند مصدر لدمج المراسلات.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### أنظر أيضا

* class [MailMerge](../../../aspose.words.mailmerging/mailmerge/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


