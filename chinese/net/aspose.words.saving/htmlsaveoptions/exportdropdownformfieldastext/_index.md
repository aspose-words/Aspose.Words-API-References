---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions ExportDropDownFormFieldAsText 财产. 控制如何将下拉表单字段保存为 HTML 或 MHTML 默认值为错误的 在 C#.
type: docs
weight: 130
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

控制如何将下拉表单字段保存为 HTML 或 MHTML。 默认值为`错误的`.

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## 评论

当设置为`真的`，将下拉表单字段导出为普通文本。 当`错误的`，将下拉表单字段导出为 HTML 中的 SELECT 元素。

导出到 EPUB 时，由于 此格式的要求，文本下拉表单字段始终保存为文本。

## 例子

演示如何在保存为 html 时使下拉组合框表单字段与段落文本混合。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用文档生成器插入一个选择了值“Two”的组合框。
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// 此 SaveOptions 对象的“ExportDropDownFormFieldAsText”标志允许我们
// 控制将文档保存为 HTML 时如何处理下拉组合框。
// 将其设置为“true”会将每个组合框转换为简单文本
// 显示组合框当前选定的值，有效地冻结它。
// 将其设置为“false”将保留使用 <select> 的组合框的功能和<选项>标签。
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
