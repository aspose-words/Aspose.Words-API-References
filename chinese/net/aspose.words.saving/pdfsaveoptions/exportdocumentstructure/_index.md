---
title: PdfSaveOptions.ExportDocumentStructure
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 获取或设置决定是否导出文档结构的值
type: docs
weight: 140
url: /zh/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

获取或设置决定是否导出文档结构的值。

```csharp
public bool ExportDocumentStructure { get; set; }
```

### 评论

保存到 PDF/A-1a、PDF/A-2a 和 PDF/UA-1 时将忽略该值，因为此合规性需要文档结构。

请注意，导出文档结构会显着增加内存消耗，尤其是 对于大型文档。

### 例子

展示如何保留文档结构元素，这可以帮助以编程方式解释我们的文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“ExportDocumentStructure”属性设置为“true”以使文档结构（例如标签）可通过
// Adobe Acrobat 的“内容”导航窗格，但代价是文件大小增加。
// 将“ExportDocumentStructure”属性设置为“false”以不导出文档结构。
options.ExportDocumentStructure = exportDocumentStructure;

// 假设我们在保存该文档时导出文档结构。在这种情况下，
// 我们可以使用 Adobe Acrobat 打开它并查找标题等元素的标签
// 通过“View”进入下一段 -> “显示/隐藏”-> “导航窗格”-> “标签”。
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


