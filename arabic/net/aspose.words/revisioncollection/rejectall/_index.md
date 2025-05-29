---
title: RevisionCollection.RejectAll
linktitle: RejectAll
articleTitle: RejectAll
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة RevisionCollection RejectAll للتخلص من جميع المراجعات بسهولة، مما يعمل على تبسيط سير عملك وتحسين إدارة المستندات.
type: docs
weight: 80
url: /ar/net/aspose.words/revisioncollection/rejectall/
---
## RevisionCollection.RejectAll method

يرفض جميع المراجعات في هذه المجموعة.

```csharp
public void RejectAll()
```

## أمثلة

يوضح كيفية العمل مع مجموعة المراجعات الخاصة بالمستند.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

//تحتوي هذه المجموعة نفسها على مجموعة من مجموعات المراجعة.
// كل مجموعة عبارة عن سلسلة من المراجعات المتجاورة.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// قم بالتكرار على مجموعة المجموعات وطباعة النص الذي يتعلق بالمراجعة.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// يحصل كل تشغيل يتأثر بالمراجعة على كائن مراجعة مطابق.
// إن مجموعة المراجعات أكبر بكثير من الشكل المكثف الذي طبعناه أعلاه،
// اعتمادًا على عدد عمليات التشغيل التي قمنا بتقسيم المستند إليها أثناء تحرير Microsoft Word.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // يؤثر تغيير تعريف النمط بشكل صارم على الأنماط، وليس على عقد المستندات. هذا يعني أن "ParentStyle"
        // ستكون الخاصية دائمًا قيد الاستخدام، بينما ستكون ParentNode دائمًا فارغة.
        // نظرًا لأن جميع التغييرات الأخرى تؤثر على العقد، فسيتم استخدام ParentNode على العكس من ذلك، وسيكون ParentStyle فارغًا.
        if (e.Current.RevisionType == RevisionType.StyleDefinitionChange)
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, style: [{e.Current.ParentStyle.Name}]");
        }
        else
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, contents: [{e.Current.ParentNode.GetText().Trim()}]");
        }
    }
}

// رفض كافة المراجعات عبر المجموعة، وإعادة المستند إلى شكله الأصلي.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### أنظر أيضا

* class [RevisionCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
