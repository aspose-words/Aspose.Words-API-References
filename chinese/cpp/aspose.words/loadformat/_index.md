---
title: "Aspose::Words::LoadFormat enum"
linktitle: "LoadFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LoadFormat enum. 指示要在 C++ 中加载的文档格式。"
type: docs
weight: 97000
url: /zh/cpp/aspose.words/loadformat/
---
## LoadFormat enum


指示要加载的文档的格式。

```cpp
enum class LoadFormat
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 自动 | 0 | 指示 Aspose.Words 自动识别格式。 |
| MsWorks | 8 | Microsoft Works 8 [Document](../document/)。 |
| Doc | 10 | Microsoft Word 95 或 Word 97 - 2003 [Document](../document/)。 |
| Dot | 11 | Microsoft Word 95 或 Word 97 - 2003 模板。 |
| DocPreWord60 | 12 | 该文档为 pre-Word 95 格式。Aspose.Words 目前不支持加载此类文档。 |
| Docx | 20 | Office Open XML WordprocessingML [Document](../document/)（无宏）。 |
| Docm | 21 | Office Open XML WordprocessingML 启用宏的 [Document](../document/)。 |
| Dotx | 22 | Office Open XML WordprocessingML 模板（无宏）。 |
| Dotm | 23 | Office Open XML WordprocessingML 宏启用模板。 |
| FlatOpc | 24 | Office Open XML WordprocessingML 存储在平面 XML 文件中，而不是 ZIP 包。 |
| FlatOpcMacroEnabled | 25 | Office Open XML WordprocessingML 宏启用 [文档](../document/) 存储在平面 XML 文件中，而不是 ZIP 包。 |
| FlatOpcTemplate | 26 | Office Open XML WordprocessingML 模板（无宏）存储在平面 XML 文件中，而不是 ZIP 包。 |
| FlatOpcTemplateMacroEnabled | 27 | Office Open XML WordprocessingML 宏启用模板存储在平面 XML 文件中，而不是 ZIP 包。 |
| Rtf | 30 | RTF 格式。 |
| WordML | 31 | Microsoft Word 2003 WordprocessingML 格式。 |
| Html | 50 | HTML 格式。 |
| Mhtml | 51 | MHTML（网页存档）格式。 |
| Mobi | 52 | MOBI 格式。用于 MobiPocket 阅读器和 Amazon Kindle 阅读器。 |
| Chm | 53 | CHM（已编译的 HTML 帮助）格式。 |
| Azw3 | 54 | AZW3 格式。用于 Amazon Kindle 阅读器。 |
| Epub | 55 | EPUB 格式。 |
| Odt | 60 | ODF 文本 [文档](../document/)。 |
| Ott | 61 | ODF 文本 [文档](../document/) 模板。 |
| 文本 | 62 | 纯文本。 |
| Markdown | 63 | Markdown 文本文档。 |
| Xml | 65 | XML 文档。 |
| Unknown | 255 | 无法识别的格式，无法由 [Aspose.Words](../) 加载。 |


## 示例



展示如何使用 [FileFormatUtil](../fileformatutil/) 方法来检测文档的格式。
```cpp
// 从缺少文件扩展名的文件加载文档，然后检测其文件格式。
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // 下面是将 LoadFormat 转换为相应 SaveFormat 的两种方法。
    // 1 - 获取 LoadFormat 的文件扩展名字符串，然后从该字符串获取相应的 SaveFormat：
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 - 直接将 LoadFormat 转换为其 SaveFormat：
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // 从流中加载文档，然后保存为自动检测的文件扩展名。
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```


展示在打开 html 文档时如何指定基础 URI。
```cpp
// 假设我们想加载一个包含相对 URI 链接图像的 .html 文档
// 而图像位于不同的位置。在这种情况下，我们需要将相对 URI 解析为绝对 URI。
// 我们可以使用 HtmlLoadOptions 对象提供基础 URI。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// 虽然图像在输入的 .html 中损坏，但我们的自定义基础 URI 帮助我们修复了链接。
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// 此输出文档将显示缺失的图像。
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
