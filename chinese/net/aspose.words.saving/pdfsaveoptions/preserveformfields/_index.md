---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words for .NET
description: 了解 PdfSaveOptions 的 PreserveFormFields 属性如何在 PDF 中保留 Microsoft Word 表单字段或将其转换为文本。提升您的文档质量！
type: docs
weight: 280
url: /zh/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

指定是否将 Microsoft Word 表单字段保留为 PDF 中的表单字段或将其转换为文本。 默认值为`错误的`.

```csharp
public bool PreserveFormFields { get; set; }
```

## 评论

Microsoft Word 表单字段包括文本输入、下拉菜单和复选框控件。

当设置为`错误的` ，这些字段将以文本形式导出为 PDF。设置为`真的`, 这些字段将被导出为 PDF 表单字段。

将表单字段作为表单字段导出为 PDF 时，可能会出现一些格式损失，因为 PDF form 字段不支持 Microsoft Word 表单字段的所有功能。

此外，输出大小取决于内容大小，因为 Microsoft Word 中的可编辑表单是 内联对象。

PDF/A 合规性禁止使用可编辑的表格。`错误的`保存为 PDF/A 时将自动使用 值。

保存为 PDF/UA 时不支持表单字段。`错误的`值将被自动使用。

## 例子

展示如何使用 Save 方法和 PdfSaveOptions 类将文档保存为 PDF 格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// 插入一个组合框，允许用户从字符串集合中选择一个选项。
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// 将“PreserveFormFields”属性设置为“true”以将表单字段保存为输出 PDF 中的交互式对象。
// 将“PreserveFormFields”属性设置为“false”，以冻结文档中的所有表单字段
// 它们的当前值并在输出 PDF 中将它们显示为纯文本。
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
