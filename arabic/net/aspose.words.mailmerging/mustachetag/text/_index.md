---
title: MustacheTag.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MustacheTag Text لاسترداد نص العلامة واستخدامه بسهولة لتحسين التعامل مع البيانات والتكامل السلس.
type: docs
weight: 30
url: /ar/net/aspose.words.mailmerging/mustachetag/text/
---
## MustacheTag.Text property

يحصل على نص العلامة.

```csharp
public string Text { get; }
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

* class [MustacheTag](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
