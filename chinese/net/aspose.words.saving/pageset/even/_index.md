---
title: PageSet.Even
linktitle: Even
articleTitle: Even
second_title: Aspose.Words for .NET
description: 使用 PageSet Even 功能，按原始顺序检索文档中的所有偶数页。简化您的工作流程，增强文档管理！
type: docs
weight: 30
url: /zh/net/aspose.words.saving/pageset/even/
---
## PageSet.Even property

获取文档所有偶数页按原始顺序排列的集合。

```csharp
public static PageSet Even { get; }
```

## 评论

偶数页具有奇数索引，因为页面索引是从零开始的。

## 例子

显示如何从文档中导出奇数页。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 5; i++)
{
    builder.Writeln($"Page {i + 1} ({(i % 2 == 0 ? "odd" : "even")})");
    if (i < 4)
        builder.InsertBreak(BreakType.PageBreak);
}

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 下面是三个 PageSet 属性，我们可以用它们来从中筛选出一组页面
// 根据页码的奇偶性将我们的文档保存在输出 PDF 文档中。
// 1 - 仅保存偶数页：
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 - 仅保存奇数页：
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 - 保存每一页：
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### 也可以看看

* class [PageSet](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
