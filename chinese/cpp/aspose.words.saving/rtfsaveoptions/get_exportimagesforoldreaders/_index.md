---
title: "Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders 方法"
linktitle: "get_ExportImagesForOldReaders"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders 方法。指定是否将 \"old readers\" 的关键字写入 RTF。此设置可能会显著影响 RTF 文档的大小。默认值在 C++ 中为 true。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/rtfsaveoptions/get_exportimagesforoldreaders/
---
## RtfSaveOptions::get_ExportImagesForOldReaders method


指定是否将针对 \"old readers\" 的关键字写入 RTF。此设置可能显著影响 RTF 文档的大小。默认值为 **true**。

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders() const
```

## 备注


"Old readers" 是指 Microsoft Word 97 之前的应用程序以及 WordPad。当此选项为 **true** 时，Aspose.Words 会写入额外的 RTF 关键字。这些关键字使文档在 "old reader" 应用程序中打开时能够正确显示，但会显著增加文档的大小。

如果将此选项设置为 **false**，则只有 WMF、EMF 和 BMP 格式的图像会在 "old readers" 中显示。

## 示例



展示如何使用自定义选项将文档保存为 .rtf。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 创建一个 \"RtfSaveOptions\" 对象并传递给文档的 \"Save\" 方法，以修改我们将其保存为 RTF 的方式。
auto options = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, options->get_SaveFormat());

// 将 \"ExportCompactSize\" 属性设置为 \"true\" 以
// 在牺牲从右到左文本兼容性的前提下减小已保存文档的大小。
options->set_ExportCompactSize(true);

// 将 \"ExportImagesFotOldReaders\" 属性设置为 \"true\" 以使用额外的关键字，确保我们的文档是
// 兼容 Microsoft Word 97 之前的阅读器和 WordPad。
// 将 \"ExportImagesFotOldReaders\" 属性设置为 \"false\" 以减小文档的大小，
// 但会阻止旧阅读器读取文档中可能包含的任何非元文件或 BMP 图像。
options->set_ExportImagesForOldReaders(exportImagesForOldReaders);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.ExportImages.rtf", options);
```

## 另见

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
