---
title: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode enum"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode enum. Anger hur Aspose.Words exporterar tomma stycken till Markdown i C++."
type: docs
weight: 66250
url: /sv/cpp/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enum


Anger hur Aspose.Words exporterar tomma stycken till Markdown.

```cpp
enum class MarkdownEmptyParagraphExportMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| EmptyLine | 0 | Exportera som tomma rader. |
| MarkdownHardLineBreak | 1 | Exportera som Markdown HardLineBreak-tecken '\'. |
| None | 2 | Exportera inte tomma stycken. |


## Exempel



Visar hur man exporterar tomma stycken.
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

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
