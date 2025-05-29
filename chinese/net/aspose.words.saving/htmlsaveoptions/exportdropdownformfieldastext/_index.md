---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: Aspose.Words for .NET
description: 了解 HtmlSaveOptions ExportDropDownFormFieldAsText 属性如何通过控制下拉字段格式来增强您的 HTML/MHTML 导出功能。优化您的文档！
type: docs
weight: 130
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

控制下拉表单字段如何保存为 HTML 或 MHTML。 默认值为`错误的`.

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## 评论

当设置为`真的`，将下拉表单字段导出为普通文本。 当`错误的`，将下拉表单字段导出为 HTML 中的 SELECT 元素。

导出为 EPUB 时，文本下拉表单字段始终保存为文本，以满足此格式的要求。

## 例子

展示如何在保存为 HTML 时使下拉组合框表单字段与段落文本混合。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用文档生成器插入一个选择值“Two”的组合框。
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// 此 SaveOptions 对象的“ExportDropDownFormFieldAsText”标志允许我们
// 控制将文档保存为 HTML 时如何处理下拉组合框。
// 将其设置为“true”将把每个组合框转换为简单文本
// 显示组合框当前选定的值，从而有效地冻结它。
// 将其设置为“false”将保留使用 <select> 和 <option> 标签的组合框的功能。
HtmlSaveOptions options = new HtmlSaveOptions();
options.ExportDropDownFormFieldAsText = exportDropDownFormFieldAsText;    

doc.Save(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
    Assert.True(outDocContents.Contains(
        "<span>Two</span>"));
else
    Assert.True(outDocContents.Contains(
        "<select name=\"MyComboBox\">" +
            "<option>One</option>" +
            "<option selected=\"selected\">Two</option>" +
            "<option>Three</option>" +
        "</select>"));
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
