---
title: HtmlFixedSaveOptions.ExportFormFields
linktitle: ExportFormFields
articleTitle: ExportFormFields
second_title: Aspose.Words for .NET
description: 了解 HtmlFixedSaveOptions ExportFormFields 属性如何通过保持表单字段交互来增强文档导出，从而改善用户体验。
type: docs
weight: 80
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/exportformfields/
---
## HtmlFixedSaveOptions.ExportFormFields property

获取或设置表单字段是否导出为交互式 项（作为“输入”标签）而不是转换为文本或图形的指示。

```csharp
public bool ExportFormFields { get; set; }
```

## 例子

展示如何将表单字段导出为 Html。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertCheckBox("CheckBox", false, 15);

// 当我们将带有表单字段的文档导出为 .html 时，
// Aspose.Words 可以通过两种方式导出表单字段。
// 将“ExportFormFields”标志设置为“true”将把它们导出为交互式对象。
// 将此标志设置为“false”将把表单字段显示为纯文本。
// 这会将它们冻结在当前值，并阻止读取我们的 HTML 文档
// 无法与他们互动。
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportFormFields = exportFormFields
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />").Success);
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"").Success);
}
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
