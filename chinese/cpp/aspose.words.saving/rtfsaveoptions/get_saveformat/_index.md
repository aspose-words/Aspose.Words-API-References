---
title: "Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat 方法"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat 方法。指定在使用此保存选项对象时文档将保存的格式。在 C++ 中只能是 Rtf。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/rtfsaveoptions/get_saveformat/
---
## RtfSaveOptions::get_SaveFormat method


指定在使用此保存选项对象时文档将保存的格式。只能是 [Rtf](../../../aspose.words/saveformat/)。

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
