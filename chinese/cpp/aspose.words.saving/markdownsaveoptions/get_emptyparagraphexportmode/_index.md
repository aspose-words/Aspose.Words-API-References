---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_EmptyParagraphExportMode 方法"
linktitle: "get_EmptyParagraphExportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_EmptyParagraphExportMode 方法。指定如何将空段落导出为 Markdown。默认值在 C++ 中为 EmptyLine。"
type: docs
weight: 2250
url: /zh/cpp/aspose.words.saving/markdownsaveoptions/get_emptyparagraphexportmode/
---
## MarkdownSaveOptions::get_EmptyParagraphExportMode method


指定如何将空段落导出为 Markdown。默认值是 [EmptyLine](../../markdownemptyparagraphexportmode/)。

```cpp
Aspose::Words::Saving::MarkdownEmptyParagraphExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_EmptyParagraphExportMode() const
```


## 示例



展示如何导出空段落。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"First");
builder->Writeln(u"\r\n\r\n\r\n");
builder->Writeln(u"Last");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_EmptyParagraphExportMode(exportMode);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.EmptyParagraphExportMode.md", saveOptions);

System::String result = System::IO::File::ReadAllText(get_ArtifactsDir() + u"MarkdownSaveOptions.EmptyParagraphExportMode.md");

switch (exportMode)
{
    case Aspose::Words::Saving::MarkdownEmptyParagraphExportMode::None:
        ASSERT_EQ(u"First\r\n\r\nLast\r\n", result);
        break;

    case Aspose::Words::Saving::MarkdownEmptyParagraphExportMode::EmptyLine:
        ASSERT_EQ(u"First\r\n\r\n\r\n\r\n\r\nLast\r\n\r\n", result);
        break;

    case Aspose::Words::Saving::MarkdownEmptyParagraphExportMode::MarkdownHardLineBreak:
        ASSERT_EQ(u"First\r\n\\\r\n\\\r\n\\\r\n\\\r\n\\\r\nLast\r\n<br>\r\n", result);
        break;

}
```

## 另见

* Enum [MarkdownEmptyParagraphExportMode](../../markdownemptyparagraphexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
