---
title: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode Enum"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode Enum. Gibt an, wie Aspose.Words leere Absätze in Markdown in C++ exportiert."
type: docs
weight: 66250
url: /de/cpp/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enum


Gibt an, wie Aspose.Words leere Absätze nach Markdown exportiert.

```cpp
enum class MarkdownEmptyParagraphExportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| EmptyLine | 0 | Als leere Zeilen exportieren. |
| MarkdownHardLineBreak | 1 | Als Markdown-HardLineBreak-Zeichen '\' exportieren. |
| Keine | 2 | Leere Absätze nicht exportieren. |


## Beispiele



Zeigt, wie leere Absätze exportiert werden.
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

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
