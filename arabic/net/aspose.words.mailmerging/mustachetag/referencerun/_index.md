---
title: MustacheTag.ReferenceRun
second_title: Aspose.Words لمراجع .NET API
description: MustacheTag ملكية. يحصل على التشغيل الذي يحتوي على بداية العلامة.
type: docs
weight: 20
url: /ar/net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

يحصل على التشغيل الذي يحتوي على بداية العلامة.

```csharp
public Run ReferenceRun { get; }
```

### أمثلة

يوضح كيفية العمل مع علامات الشارب.

```csharp
Document document = new Document(MyDir + "Mail merge mustache tags.docx");
document.MailMerge.UseNonMergeFields = true;

MailMergeRegionInfo hierarchy = document.MailMerge.GetRegionsHierarchy();

foreach (MustacheTag mustacheTag in hierarchy.MustacheTags)
{
    Console.WriteLine(mustacheTag.Text);
    Console.WriteLine(mustacheTag.ReferenceOffset);
    Console.WriteLine(mustacheTag.ReferenceRun);
}

foreach (MailMergeRegionInfo region in hierarchy.Regions)
{
    Console.WriteLine(region.StartMustacheTag.Text);
    Console.WriteLine(region.EndMustacheTag.Text);
}
```

### أنظر أيضا

* class [Run](../../../aspose.words/run/)
* class [MustacheTag](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mustachetag/)
* المجسم [Aspose.Words](../../../)


