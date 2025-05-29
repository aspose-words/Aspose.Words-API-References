---
title: Document.MailMerge
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words لـ .NET
description: قم بإلغاء قفل أتمتة المستندات بسلاسة باستخدام كائن MailMerge، مما يعزز سير عملك من خلال تبسيط مهام دمج البريد دون عناء.
type: docs
weight: 270
url: /ar/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

يعيد[`MailMerge`](../../../aspose.words.mailmerging/mailmerge/) الكائن الذي يمثل وظيفة دمج البريد للمستند.

```csharp
public MailMerge MailMerge { get; }
```

## أمثلة

يوضح كيفية تنفيذ دمج البريد باستخدام البيانات من جدول البيانات.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // فيما يلي طريقتان لاستخدام جدول البيانات كمصدر بيانات لدمج البريد.
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريدي واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند دمج بريدي واحد:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// إنشاء مستند مصدر لدمج البريد.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
