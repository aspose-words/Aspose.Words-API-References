---
title: FixedPageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words for .NET
description: 使用 FixedPageSaveOptions PageSet 控制文档渲染。轻松选择特定页面或全部选择以实现无缝输出。优化您的工作流程！
type: docs
weight: 70
url: /zh/net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

获取或设置要呈现的页面。 默认为文档中的所有页面。

```csharp
public PageSet PageSet { get; set; }
```

## 例子

展示如何根据精确的页面索引提取页面。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 向文档添加五页。
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// 创建一个“XpsSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .XPS 的方式。
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// 使用“PageSet”属性选择一组文档页面来保存到输出 XPS。
// 在这种情况下，我们将通过从零开始的索引仅选择三页：第 1 页、第 2 页和第 4 页。
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

展示如何将文档中的部分页面转换为 PDF。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改该方法将文档转换为 .PDF 的方式。
    PdfSaveOptions options = new PdfSaveOptions();

    // 将“PageIndex”设置为“1”以从第二页开始呈现文档的一部分。
    options.PageSet = new PageSet(1);

    // 本文档将包含从第二页开始的一页，其中只包含第二页。
    doc.Save(stream, options);
}
```

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

* class [PageSet](../../pageset/)
* class [FixedPageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
