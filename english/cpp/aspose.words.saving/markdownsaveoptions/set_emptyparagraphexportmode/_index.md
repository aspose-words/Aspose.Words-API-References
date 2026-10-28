---
title: Aspose::Words::Saving::MarkdownSaveOptions::set_EmptyParagraphExportMode method
linktitle: set_EmptyParagraphExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::set_EmptyParagraphExportMode method. Specifies how to export empty paragraphs to Markdown. Default value is EmptyLine in C++.'
type: docs
weight: 10250
url: /cpp/aspose.words.saving/markdownsaveoptions/set_emptyparagraphexportmode/
---
## MarkdownSaveOptions::set_EmptyParagraphExportMode method


Specifies how to export empty paragraphs to Markdown. Default value is [EmptyLine](../../markdownemptyparagraphexportmode/).

```cpp
void Aspose::Words::Saving::MarkdownSaveOptions::set_EmptyParagraphExportMode(Aspose::Words::Saving::MarkdownEmptyParagraphExportMode value)
```

## Examples


Shows how to export empty paragraphs.

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
    case MarkdownEmptyParagraphExportMode::None:
        ASSERT_EQ(u"First\r\n\r\nLast\r\n", result);
        break;
    case MarkdownEmptyParagraphExportMode::EmptyLine:
        ASSERT_EQ(u"First\r\n\r\n\r\n\r\n\r\nLast\r\n\r\n", result);
        break;
    case MarkdownEmptyParagraphExportMode::MarkdownHardLineBreak:
        ASSERT_EQ(u"First\r\n\\\r\n\\\r\n\\\r\n\\\r\n\\\r\nLast\r\n<br>\r\n", result);
        break;
}
```
## See Also

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
