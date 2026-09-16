---
title: "Aspose::Words::Saving::MarkdownLinkExportMode 枚举"
linktitle: "MarkdownLinkExportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownLinkExportMode 枚举。指定在 C++ 中链接如何导出为 Markdown。"
type: docs
weight: 67000
url: /zh/cpp/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enum


指定链接如何导出为 Markdown。

```cpp
enum class MarkdownLinkExportMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 自动 | 0 | 自动检测每个链接的导出模式。 |
| Inline | 1 | 将所有链接导出为内联块。 |
| 引用 | 2 | 将所有链接导出为引用块。 |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
