---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields 方法"
linktitle: "get_ExportFormFields"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields 方法。获取或设置是否将表单字段导出为交互式项目（作为 ''input'' 标签），而不是在 C++ 中转换为文本或图形。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportformfields/
---
## HtmlFixedSaveOptions::get_ExportFormFields method


获取或设置指示是否将表单字段导出为交互式项目（作为 'input' 标签），而不是转换为文本或图形。

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields() const
```


## 示例



展示如何将表单字段导出为 Html。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertCheckBox(u"CheckBox", false, 15);

// 当我们将包含表单字段的文档导出为 .html 时，
// Aspose.Words 有两种方式可以导出表单字段。
// 将 \"ExportFormFields\" 标志设置为 \"true\" 将把它们导出为交互式对象。
// 将此标志设置为 \"false\" 将把表单字段显示为纯文本。
// 这将使它们冻结在当前值，并阻止我们 HTML 文档的阅读器
// 与它们进行交互。
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportFormFields(exportFormFields);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"")->get_Success());
}
```

## 另见

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
