---
title: MailMerge.MailMergeCallback
linktitle: MailMergeCallback
articleTitle: MailMergeCallback
second_title: Aspose.Words لـ .NET
description: حسّن دمج البريد باستخدام خاصية MailMergeCallback. أدر الأحداث بسهولة لأتمتة مستنداتك بسلاسة وكفاءة أعلى.
type: docs
weight: 40
url: /ar/net/aspose.words.mailmerging/mailmerge/mailmergecallback/
---
## MailMerge.MailMergeCallback property

يسمح بالتعامل مع أحداث معينة أثناء دمج البريد.

```csharp
public IMailMergeCallback MailMergeCallback { get; set; }
```

## أمثلة

يوضح كيفية تحديد منطق مخصص للتعامل مع الأحداث أثناء دمج البريد.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // إدراج علامتي دمج بريد تشيران إلى عمودين في مصدر بيانات.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // قم بإنشاء مصدر بيانات يحتوي فقط على أحد الأعمدة التي تشير إليها علامات الدمج الخاصة بنا.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // قم بتكوين دمج البريد الخاص بنا لاستخدام علامات دمج البريد البديلة.
    doc.MailMerge.UseNonMergeFields = true;

    // ثم تأكد من أن دمج البريد سيحول العلامات، مثل علامة "LastName" الخاصة بنا،
    // في MERGEFIELDs في مستندات الدمج.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// يحسب عدد المرات التي يستبدل فيها دمج البريد علامات دمج البريد التي لا يمكنه ملؤها بالبيانات باستخدام MERGEFIELDs.
/// </summary>
private class MailMergeTagReplacementCounter : IMailMergeCallback
{
    public void TagsReplaced()
    {
        TagsReplacedCount++;
    }

    public int TagsReplacedCount { get; private set; }
}
```

### أنظر أيضا

* interface [IMailMergeCallback](../../imailmergecallback/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
