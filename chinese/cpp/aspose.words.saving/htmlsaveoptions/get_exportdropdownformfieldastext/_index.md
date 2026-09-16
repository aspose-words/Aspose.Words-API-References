---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText 方法"
linktitle: "get_ExportDropDownFormFieldAsText"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText 方法。控制下拉表单字段如何保存为 HTML 或 MHTML。默认值在 C++ 中为 false。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportdropdownformfieldastext/
---
## HtmlSaveOptions::get_ExportDropDownFormFieldAsText method


控制下拉表单字段保存到 HTML 或 MHTML 的方式。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText() const
```

## 备注


当设置为 **true** 时，导出下拉表单字段为普通文本。当设置为 **false** 时，导出下拉表单字段为 HTML 中的 SELECT 元素。

导出为 EPUB 时，文本下拉表单字段始终保存为文本，因为此格式的要求。

## 示例



展示如何在保存为 HTML 时，使下拉组合框表单字段与段落文本融合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用文档生成器插入一个选中值为 \"Two\" 的组合框。
builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"One", u"Two", u"Three"}), 1);

// 此 SaveOptions 对象的 \"ExportDropDownFormFieldAsText\" 标志允许我们
// 控制将文档保存为 HTML 时如何处理下拉组合框。
// 将其设置为 \"true\" 将把每个组合框转换为简单文本
// 该文本显示组合框当前选中的值，从而实际上冻结了它。
// 将其设置为 \"false\" 将使用 <select> 和 <option> 标记保留组合框的功能。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportDropDownFormFieldAsText(exportDropDownFormFieldAsText);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Two</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<select name=\"MyComboBox\">") + u"<option>One</option>" + u"<option selected=\"selected\">Two</option>" + u"<option>Three</option>" + u"</select>"));
}
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
