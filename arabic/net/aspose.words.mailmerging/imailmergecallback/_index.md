---
title: IMailMergeCallback Interface
linktitle: IMailMergeCallback
articleTitle: IMailMergeCallback
second_title: Aspose.Words لـ .NET
description: حسّن عملية دمج البريد لديك باستخدام Aspose.Words.MailMerging.IMailMergeCallback. احصل على إشعارات فورية وحسّن كفاءة أتمتة مستنداتك.
type: docs
weight: 4490
url: /ar/net/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد تلقي الإشعارات أثناء تنفيذ دمج البريد.

```csharp
public interface IMailMergeCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [TagsReplaced](../../aspose.words.mailmerging/imailmergecallback/tagsreplaced/)() | يتم استدعاؤها عند استبدال علامات النص "mustache" بحقول MERGEFIELD. |

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

* مساحة الاسم [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../)
