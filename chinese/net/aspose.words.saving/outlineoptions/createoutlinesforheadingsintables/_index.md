---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: 用于 .NET 的 Aspose.Words
description: OutlineOptions CreateOutlinesForHeadingsInTables 财产. 指定是否为表格内的标题使用标题样式格式化的段落创建轮廓 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

指定是否为表格内的标题（使用标题样式格式化的段落）创建轮廓。

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## 评论

默认值为`错误的`。

## 例子

展示如何为表格内的标题创建 PDF 文档大纲条目。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个包含三行的表。第一行，
// 我们将其文本格式化为标题类型样式，将用作列标题。
builder.StartTable();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("Customers");
builder.EndRow();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Write("John Doe");
builder.EndRow();
builder.InsertCell();
builder.Write("Jane Doe");
builder.EndTable();

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// 输出的 PDF 文档将包含一个大纲，它是列出文档正文中的标题的目录。
// 单击此大纲中的条目将带我们到达其各自标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“1”以获取大纲
// 仅注册标题级别不大于 1 的标题。
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// 将“CreateOutlinesForHeadingsInTables”属性设置为“false”以排除表中的所有标题，
// 例如我们在上面根据大纲创建的那个。
// 将“CreateOutlinesForHeadingsInTables”属性设置为“true”以包含表中的所有标题
// 在大纲中，前提是它们的标题级别不大于“HeadingsOutlineLevels”属性的值。
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### 也可以看看

* class [OutlineOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
