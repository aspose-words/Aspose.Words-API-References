---
title: MustacheTag.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: 探索 MustacheTag Text 属性，轻松检索和利用标签文本，以增强数据处理和无缝集成。
type: docs
weight: 30
url: /zh/net/aspose.words.mailmerging/mustachetag/text/
---
## MustacheTag.Text property

获取标签的文本。

```csharp
public string Text { get; }
```

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

* class [MustacheTag](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
