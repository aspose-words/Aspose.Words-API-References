---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting 方法"
linktitle: "get_ExportUnderlineFormatting"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting 方法。获取或设置一个布尔值，指示是否将下划线文本格式导出为两个加号 \"++\" 的序列。默认值在 C++ 中为 false。"
type: docs
weight: 3500
url: /zh/cpp/aspose.words.saving/markdownsaveoptions/get_exportunderlineformatting/
---
## MarkdownSaveOptions::get_ExportUnderlineFormatting method


获取或设置一个布尔值，指示是否将下划线文本格式导出为两个加号 "++" 的序列。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting() const
```


## 示例



展示如何将下划线格式导出为 ++。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Single);
builder->Write(u"Lorem ipsum. Dolor sit amet.");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportUnderlineFormatting(true);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

## 另见

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
