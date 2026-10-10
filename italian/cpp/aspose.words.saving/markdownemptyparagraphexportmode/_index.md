---
title: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode enum"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode enum. Specifica come Aspose.Words esporta i paragrafi vuoti in Markdown in C++."
type: docs
weight: 66250
url: /it/cpp/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enum


Specifica come Aspose.Words esporta i paragrafi vuoti in Markdown.

```cpp
enum class MarkdownEmptyParagraphExportMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| EmptyLine | 0 | Esporta come linee vuote. |
| MarkdownHardLineBreak | 1 | Esporta come carattere Markdown HardLineBreak '\'. |
| None | 2 | Non esportare i paragrafi vuoti. |


## Esempi



Mostra come esportare i paragrafi vuoti.
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

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
