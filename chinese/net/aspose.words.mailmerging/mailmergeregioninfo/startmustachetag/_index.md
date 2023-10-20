---
title: MailMergeRegionInfo.StartMustacheTag
linktitle: StartMustacheTag
articleTitle: StartMustacheTag
second_title: 用于 .NET 的 Aspose.Words
description: MailMergeRegionInfo StartMustacheTag 财产. 返回该区域的开始mustache标签 在 C#.
type: docs
weight: 100
url: /zh/net/aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/
---
## MailMergeRegionInfo.StartMustacheTag property

返回该区域的开始“mustache”标签。

```csharp
public MustacheTag StartMustacheTag { get; }
```

## 例子

展示如何使用小胡子标签。

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

### 也可以看看

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
