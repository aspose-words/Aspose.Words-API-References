---
title: MustacheTag Class
linktitle: MustacheTag
articleTitle: MustacheTag
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.MailMerging.MustacheTag—تعامل بكفاءة مع علامات mustache لأتمتة المستندات بسلاسة وتحسين دمج البريد.
type: docs
weight: 4570
url: /ar/net/aspose.words.mailmerging/mustachetag/
---
## MustacheTag class

يمثل علامة "الشارب".

```csharp
public class MustacheTag
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [ReferenceOffset](../../aspose.words.mailmerging/mustachetag/referenceoffset/) { get; } | يحصل على موضع البداية المستند إلى الصفر للعلامة من بداية[`ReferenceRun`](./referencerun/) . |
| [ReferenceRun](../../aspose.words.mailmerging/mustachetag/referencerun/) { get; } | يحصل على التشغيل الذي يحتوي على بداية العلامة. |
| [Text](../../aspose.words.mailmerging/mustachetag/text/) { get; } | يحصل على نص العلامة. |

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

* مساحة الاسم [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../)
