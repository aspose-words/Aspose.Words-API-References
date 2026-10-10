---
title: "Aspose::Words::Document::Save 方法"
linktitle: "保存"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::Save 方法。使用指定的格式在 C++ 中将文档保存到流。"
type: docs
weight: 72000
url: /zh/cpp/aspose.words/document/save/
---
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


使用指定的格式将文档保存到流中。

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | 用于保存文档的流。 |
| saveFormat | Aspose::Words::SaveFormat | 保存文档的格式。 |

### ReturnValue

您可以选择使用的附加信息。

## 示例



展示如何通过流将文档保存为图像，然后从该流读取图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");
```


展示如何将文档保存到流中。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

{
    auto dstStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(dstStream, Aspose::Words::SaveFormat::Docx);

    // 验证流中包含该文档。
    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", System::MakeObject<Aspose::Words::Document>(dstStream)->GetText().Trim());
}
```

## 另见

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


使用指定的保存选项将文档保存到流中。

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | 用于保存文档的流。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 指定控制文档保存方式的选项。可以为 **null**。如果为 **null**，文档将以二进制 DOC 格式保存。 |

### ReturnValue

您可以选择使用的附加信息。

## 另见

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&) method


将文档保存到文件。自动根据扩展名确定保存格式。

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 文档的名称。如果具有指定文件名的文档已存在，则会覆盖现有文档。 |

### ReturnValue

您可以选择使用的附加信息。

## 示例



展示如何打开文档并将其转换为 .PDF。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## 另见

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, Aspose::Words::SaveFormat) method


以指定格式将文档保存到文件。

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 文档的名称。如果具有指定文件名的文档已存在，则会覆盖现有文档。 |
| saveFormat | Aspose::Words::SaveFormat | 保存文档的格式。 |

### ReturnValue

您可以选择使用的附加信息。

## 示例



展示如何将 DOCX 转换为 HTML 格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## 另见

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


使用指定的保存选项将文档保存到文件。

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 文档的名称。如果具有指定文件名的文档已存在，则会覆盖现有文档。 |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | 指定控制文档保存方式的选项。可以为 **null**。 |

### ReturnValue

您可以选择使用的附加信息。

## 示例



展示如何使用 SaveOptions 提升渲染文档的质量。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```


展示如何将文档中的单页渲染为 JPEG 图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// 创建一个 "ImageSaveOptions" 对象，以便将其传递给文档的 "Save" 方法。
// 以修改该方法将文档渲染为图像的方式。
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// 将 "PageSet" 设置为 "1" 以通过
// 零基索引来指定文档渲染的起始页。
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// 当我们将文档保存为 JPEG 格式时，Aspose.Words 只渲染一页。
// 此图像将包含从第二页开始的单页，
// 这将仅是原始文档的第二页。
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```


展示如何将文档的每一页渲染为单独的 TIFF 图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// 创建一个 "ImageSaveOptions" 对象，以便将其传递给文档的 "Save" 方法。
// 以修改该方法将文档渲染为图像的方式。
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // 将 "PageSet" 属性设置为起始页的页码，从
    // 该页开始渲染文档。
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // 以 2325x5325 像素、600 dpi 导出页面。
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```


展示如何在将文档保存为 JPEG 时配置压缩。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 创建一个 "ImageSaveOptions" 对象，以便将其传递给文档的 "Save" 方法。
// 以修改该方法将文档渲染为图像的方式。
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// 将 "JpegQuality" 属性设置为 "10"，以在渲染文档时使用更强的压缩。
// 这将减小文档的文件大小，但图像会出现更明显的压缩伪影。
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// 将 "JpegQuality" 属性设置为 "100"，以在渲染文档时使用较弱的压缩。
// 这将提升图像质量，但会导致文件大小增加。
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## 另见

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, Aspose::Words::SaveFormat saveFormat)
```

## 另见

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)
```

## 另见

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
