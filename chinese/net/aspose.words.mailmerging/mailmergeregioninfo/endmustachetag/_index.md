---
title: MailMergeRegionInfo.EndMustacheTag
second_title: Aspose.Words for .NET API 参考
description: MailMergeRegionInfo 财产. 返回该区域的结束mustache标签
type: docs
weight: 20
url: /zh/net/aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/
---
## MailMergeRegionInfo.EndMustacheTag property

返回该区域的结束“mustache”标签。

```csharp
public MustacheTag EndMustacheTag { get; }
```

### 例子

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
* 命名空间 [Aspose.Words.MailMerging](../../mailmergeregioninfo/)
* 部件 [Aspose.Words](../../../)


