---
title: MailMergeRegionInfo.EndMustacheTag
second_title: Aspose.Words لمراجع .NET API
description: MailMergeRegionInfo ملكية. إرجاع علامة نهاية الشارب للمنطقة.
type: docs
weight: 20
url: /ar/net/aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/
---
## MailMergeRegionInfo.EndMustacheTag property

إرجاع علامة نهاية "الشارب" للمنطقة.

```csharp
public MustacheTag EndMustacheTag { get; }
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

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmergeregioninfo/)
* المجسم [Aspose.Words](../../../)


