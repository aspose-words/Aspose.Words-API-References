---
title: Revision.ParentStyle
linktitle: ParentStyle
articleTitle: ParentStyle
second_title: Aspose.Words لـ .NET
description: Revision ParentStyle ملكية. يحصل على النمط الأصلي المباشر المالك لهذه المراجعة. ستعمل هذه الخاصية فقط معStyleDefinitionChange نوع المراجعة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words/revision/parentstyle/
---
## Revision.ParentStyle property

يحصل على النمط الأصلي المباشر (المالك) لهذه المراجعة. ستعمل هذه الخاصية فقط معStyleDefinitionChange نوع المراجعة.

```csharp
public Style ParentStyle { get; }
```

## ملاحظات

إذا كانت هذه المراجعة تتعلق بالتغييرات في عقد المستند، فاستخدم[`ParentNode`](../parentnode/) بدلا من ذلك.

## أمثلة

يوضح كيفية التعامل مع مجموعة مراجعات المستند.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// تحتوي هذه المجموعة نفسها على مجموعة من مجموعات المراجعة.
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

// كل عملية تشغيل تؤثر عليها المراجعة تحصل على كائن مراجعة مطابق.
// مجموعة المراجعات أكبر بكثير من النموذج الموجز الذي طبعناه أعلاه،
// اعتمادًا على عدد مرات التشغيل التي قمنا بتقسيم المستند إليها أثناء تحرير Microsoft Word.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // يؤثر StyleDefinitionChange بشكل صارم على الأنماط وليس على عقد المستند. وهذا يعني "ParentStyle"
        ستكون الخاصية // قيد الاستخدام دائمًا، بينما ستكون ParentNode فارغة دائمًا.
        // نظرًا لأن جميع التغييرات الأخرى تؤثر على العقد، فسيتم استخدام ParentNode على العكس من ذلك، وسيكون ParentStyle خاليًا.
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

// رفض جميع المراجعات عبر المجموعة، مما يعيد المستند إلى شكله الأصلي.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### أنظر أيضا

* class [Style](../../style/)
* class [Revision](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
