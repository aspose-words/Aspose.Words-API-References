---
title: MustacheTag Class
linktitle: MustacheTag
articleTitle: MustacheTag
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.MailMerging.MustacheTag 类 - 有效处理胡须标签，实现无缝文档自动化和增强邮件合并。
type: docs
weight: 4570
url: /zh/net/aspose.words.mailmerging/mustachetag/
---
## MustacheTag class

代表“胡子”标签。

```csharp
public class MustacheTag
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ReferenceOffset](../../aspose.words.mailmerging/mustachetag/referenceoffset/) { get; } | 从标签的开头获取从零开始的起始位置[`ReferenceRun`](./referencerun/). |
| [ReferenceRun](../../aspose.words.mailmerging/mustachetag/referencerun/) { get; } | 获取包含标签开头的运行。 |
| [Text](../../aspose.words.mailmerging/mustachetag/text/) { get; } | 获取标签的文本。 |

## 例子

展示如何使用胡子标签。

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

* 命名空间 [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../)
