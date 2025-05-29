---
title: PdfSaveOptions.RenderChoiceFormFieldBorder
linktitle: RenderChoiceFormFieldBorder
articleTitle: RenderChoiceFormFieldBorder
second_title: Aspose.Words for .NET
description: 了解 PdfSaveOptions RenderChoiceFormFieldBorder 属性如何通过控制选择字段边框来增强 PDF 表单设计，从而提供更好的用户体验。
type: docs
weight: 290
url: /zh/net/aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/
---
## PdfSaveOptions.RenderChoiceFormFieldBorder property

指定是否呈现 PDF 选择表单字段边框。

```csharp
public bool RenderChoiceFormFieldBorder { get; set; }
```

## 评论

PDF 选择表单字段用于导出 SDT 组合框内容控件、SDT 下拉列表内容 控件和旧式下拉表单字段[`PreserveFormFields`](../preserveformfields/)选项已启用。

默认值为`真的`。

## 例子

展示如何呈现 PDF 选择表单字段边框。

```csharp
Document doc = new Document(MyDir + "Legacy drop-down.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
saveOptions.RenderChoiceFormFieldBorder = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderChoiceFormFieldBorder.pdf", saveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
