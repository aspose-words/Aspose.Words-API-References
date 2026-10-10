---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins 方法"
linktitle: "get_ExportPageMargins"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins 方法。指定是否将页面边距导出到 HTML、MHTML 或 EPUB。默认在 C++ 中为 false。"
type: docs
weight: 23000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagemargins/
---
## HtmlSaveOptions::get_ExportPageMargins method


指定是否将页面边距导出到 HTML、MHTML 或 EPUB。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins() const
```


## 示例



展示如何在输出的 HTML 文档中显示超出边界的对象。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用构建器插入一个没有换行的形状。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 200, 200);

shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// 负的形状位置值可能会将形状放置在页面边界之外。
// 如果我们将其导出为 HTML，形状将会被截断。
shape->set_Left(-150);

// 在将文档保存为 HTML 时，我们可以传入一个 SaveOptions 对象
// 以决定是否调整页面以完整显示超出边界的对象。
// 如果我们将 "ExportPageMargins" 标志设置为 "true"，形状将在输出的 HTML 中完整可见。
// 如果我们将 "ExportPageMargins" 标志设置为 "false",
// 我们的文档将显示被截断的形状，正如在 Microsoft Word 中看到的那样。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageMargins(exportPageMargins);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    ASSERT_TRUE(outDocContents.Contains(u"<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    ASSERT_TRUE(outDocContents.Contains(u"<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
