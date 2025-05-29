---
title: SaveOptions.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words for .NET
description: 了解 SaveOptions 的 UpdateFields 属性如何通过在转换为固定格式之前更新特定字段类型来优化文档保存。默认值为 true。
type: docs
weight: 170
url: /zh/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为`真的`.

```csharp
public bool UpdateFields { get; set; }
```

## 评论

允许指定是否模仿 MS Word 行为。

## 例子

展示如何在将文档保存为 PDF 之前立即更新文档中的所有字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入包含 PAGE 和 NUMPAGES 字段的文本。这些字段无法实时显示正确的值。
// 我们需要使用更新方法（例如“Field.Update()”和“Document.UpdateFields()”）手动更新它们
// 每次我们都需要它们显示准确的值。
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“UpdateFields”属性设置为“false”以在保存操作之前不更新文档中的所有字段。
// 如果我们知道在保存之前所有字段都是最新的，那么这是更好的选择。
// 将“UpdateFields”属性设置为“true”以遍历所有文档
// 字段，并在保存为 PDF 之前更新它们。这将确保所有字段都显示
// PDF 中最准确的值。
options.UpdateFields = updateFields;

// 我们可以克隆 PdfSaveOptions 对象。
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
