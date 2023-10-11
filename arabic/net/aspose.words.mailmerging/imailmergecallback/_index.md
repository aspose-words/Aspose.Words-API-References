---
title: Interface IMailMergeCallback
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.MailMerging.IMailMergeCallback واجهه المستخدم. قم بتطبيق هذه الواجهة إذا كنت تريد تلقي إشعارات أثناء إجراء دمج البريد.
type: docs
weight: 3800
url: /ar/net/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface

قم بتطبيق هذه الواجهة إذا كنت تريد تلقي إشعارات أثناء إجراء دمج البريد.

```csharp
public interface IMailMergeCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [TagsReplaced](../../aspose.words.mailmerging/imailmergecallback/tagsreplaced/)() | يتم الاتصال به عند استبدال العلامات النصية "الشارب" بحقول MERGEFIELD. |

### أمثلة

يوضح كيفية تحديد المنطق المخصص للتعامل مع الأحداث أثناء دمج البريد.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل علامتي دمج المراسلات تشيران إلى عمودين في مصدر بيانات.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // قم بإنشاء مصدر بيانات يحتوي فقط على أحد الأعمدة التي تشير إليها علامات الدمج الخاصة بنا.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // قم بتكوين دمج البريد الخاص بنا لاستخدام علامات دمج البريد البديلة.
    doc.MailMerge.UseNonMergeFields = true;

    // بعد ذلك، تأكد من أن عملية دمج البريد ستحول العلامات، مثل علامة "LastName" الخاصة بنا،
    // إلى MERGEFIELDs في مستندات الدمج.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// حساب عدد المرات التي يستبدل فيها دمج البريد علامات دمج البريد التي لم يتمكن من تعبئتها بالبيانات باستخدام MERGEFIELDs.
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


