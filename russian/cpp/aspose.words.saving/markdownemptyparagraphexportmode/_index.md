---
title: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode перечисление"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode перечисление. Указывает, как Aspose.Words экспортирует пустые абзацы в Markdown в C++."
type: docs
weight: 66250
url: /ru/cpp/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enum


Указывает, как Aspose.Words экспортирует пустые абзацы в Markdown.

```cpp
enum class MarkdownEmptyParagraphExportMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| EmptyLine | 0 | Экспортировать как пустые строки. |
| MarkdownHardLineBreak | 1 | Экспортировать как символ разрыва строки Markdown HardLineBreak '\'. |
| None | 2 | Не экспортировать пустые абзацы. |


## Примеры



Показывает, как экспортировать пустые абзацы.
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

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
