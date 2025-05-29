---
title: PdfSaveOptions.UseSdtTagAsFormFieldName
linktitle: UseSdtTagAsFormFieldName
articleTitle: UseSdtTagAsFormFieldName
second_title: Aspose.Words for .NET
description: 了解 PdfSaveOptions UseSdtTagAsFormFieldName 属性如何通过使用 SDT 控制标签来增强 PDF 表单的组织性和清晰度。
type: docs
weight: 340
url: /zh/net/aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/
---
## PdfSaveOptions.UseSdtTagAsFormFieldName property

指定是否使用 SDT 控件标签或 Id 属性作为 PDF 中表单字段的名称。

```csharp
public bool UseSdtTagAsFormFieldName { get; set; }
```

## 评论

默认值为`错误的`。

当设置为`错误的`，SDT 控件 Id 属性用作 PDF 中表单字段的名称。

当设置为`真的`，SDT 控件的标签属性用作 PDF 中表单字段的名称。

如果设置为`真的`并且Tag为空，Id属性将作为表单字段名称。

如果设置为`真的`并且标签值不是唯一的，重复的标签值将被更改为 build 唯一的 PDF 表单字段名称。

## 例子

展示如何使用 SDT 控件标签或 Id 属性作为 PDF 中表单字段的名称。

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
// 当设置为“false”时，SDT 控件 Id 属性将用作 PDF 中表单字段的名称。
// 设置为“true”时，SDT 控件标签属性将用作 PDF 中表单字段的名称。
saveOptions.UseSdtTagAsFormFieldName = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.SdtTagAsFormFieldName.pdf", saveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
