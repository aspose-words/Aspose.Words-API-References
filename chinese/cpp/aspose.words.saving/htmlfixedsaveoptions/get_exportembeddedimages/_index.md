---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages 方法"
linktitle: "get_ExportEmbeddedImages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages 方法。指定是否应以 Base64 格式将图像嵌入到 Html 文档中。请注意，设置此标志可能会显著增加输出 Html 文件的大小（在 C++ 中）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedimages/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedImages method


指定是否应以 Base64 格式将图像嵌入 Html 文档。请注意，设置此标志可能会显著增加输出 Html 文件的大小。

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages() const
```


## 示例



展示如何确定在将文档导出为 Html 时图像的存储位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// 当我们将带有嵌入图像的文档导出为 .html 时，
// Aspose.Words 可以将图像放置在两种可能的位置。
// 将 "ExportEmbeddedImages" 标志设置为 "true" 将存储原始数据
// 对于输出 HTML 文档中的所有图像，存放在 <image> 标签的 "src" 属性中。
// 将此标志设置为 "false" 将为每个图像在本地文件系统中创建一个图像文件，
// 并将所有这些文件存储在一个单独的文件夹中。
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedImages(exportImages);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" ") + u"src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />")->get_Success());
}
```

## 另见

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
