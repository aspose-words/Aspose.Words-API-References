---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode 方法"
linktitle: "get_LinkExportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode 方法。指定链接将在输出文件中的写入方式。默认值在 C++ 中为 Auto。"
type: docs
weight: 5750
url: /zh/cpp/aspose.words.saving/markdownsaveoptions/get_linkexportmode/
---
## MarkdownSaveOptions::get_LinkExportMode method


指定链接将在输出文件中的写入方式。默认值为 [Auto](../../markdownlinkexportmode/)。

```cpp
Aspose::Words::Saving::MarkdownLinkExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode() const
```


## 示例



展示链接将如何写入 .md 文件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 100, 100);

// 图像将作为引用写入：
// ![ref1]
// [ref1]: aw_ref.001.png
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Reference);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// 图像将以内联方式写入：
// ![](aw_inline.001.png)
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Inline);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

## 另见

* Enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
