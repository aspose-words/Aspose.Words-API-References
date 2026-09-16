---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf 方法"
linktitle: "get_ConvertSvgToEmf"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf 方法。获取或设置一个值，指示是否将已加载的 SVG 图像转换为 EMF 格式。默认值为 false，并且在可能的情况下，已加载的 SVG 图像将在 C++ 中保持原样存储，不进行转换。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.loading/htmlloadoptions/get_convertsvgtoemf/
---
## HtmlLoadOptions::get_ConvertSvgToEmf method


获取或设置指示是否将已加载的 SVG 图像转换为 EMF 格式的值。默认值为 **false**，如果可能，已加载的 SVG 图像将保持原样存储而不进行转换。

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf() const
```

## 备注


更新的 MS Word 版本原生支持 SVG 图像。如果加载选项中指定的 MS Word 版本支持 SVG，Aspose.Words 将保持 SVG 图像原样存储，不进行转换。如果不支持 SVG，已加载的 SVG 图像将被转换为 EMF 格式。

但是，如果此选项设置为 **true**，Aspose.Words 将把加载的 SVG 图像转换为 EMF，即使指定版本的 MS Word 已支持 SVG 图像。

## 示例



展示在保存 HTML 文档时如何将 SVG 对象转换为其他格式。
```cpp
System::String html = u"<html>\r\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\r\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\r\n                    </svg>\r\n                </html>";

// 使用 'ConvertSvgToEmf' 恢复旧行为
// 其中所有从 HTML 文档加载的 SVG 图像都会被转换为 EMF。
// 现在 SVG 图像加载时不进行转换
// 如果加载选项中指定的 MS Word 版本本地支持 SVG 图像。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_ConvertSvgToEmf(true);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), loadOptions);

// 此文档包含一个以文本形式呈现的 <svg> 元素。
// 当我们将文档保存为 HTML 时，可以传入一个 SaveOptions 对象
// 以确定保存操作如何处理该对象。
// 将 "MetafileFormat" 属性设置为 "HtmlMetafileFormat.Png" 以将其转换为 PNG 图像。
// 将 "MetafileFormat" 属性设置为 "HtmlMetafileFormat.Svg" 以保持其为 SVG 对象。
// 将 "MetafileFormat" 属性设置为 "HtmlMetafileFormat.EmfOrWmf" 以将其转换为元文件。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_MetafileFormat(htmlMetafileFormat);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case Aspose::Words::Saving::HtmlMetafileFormat::Png:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::Svg:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::EmfOrWmf:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

}
```

## 另见

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
