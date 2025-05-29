---
title: MailMergeRegionInfo.StartMustacheTag
linktitle: StartMustacheTag
articleTitle: StartMustacheTag
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StartMustacheTag في MailMergeRegionInfo، والتي توفر علامة بداية أساسية لمناطق المستندات السلسة في مشاريعك.
type: docs
weight: 100
url: /ar/net/aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/
---
## MailMergeRegionInfo.StartMustacheTag property

يعيد علامة "mustache" البداية للمنطقة.

```csharp
public MustacheTag StartMustacheTag { get; }
```

## أمثلة

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
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
