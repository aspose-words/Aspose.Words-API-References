---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_EmptyParagraphExportMode metodo"
linktitle: "get_EmptyParagraphExportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_EmptyParagraphExportMode metodo. Specifica come esportare i paragrafi vuoti in Markdown. Il valore predefinito è EmptyLine in C++."
type: docs
weight: 2250
url: /it/cpp/aspose.words.saving/markdownsaveoptions/get_emptyparagraphexportmode/
---
## MarkdownSaveOptions::get_EmptyParagraphExportMode method


Specifica come esportare i paragrafi vuoti in Markdown. Il valore predefinito è [EmptyLine](../../markdownemptyparagraphexportmode/).

```cpp
Aspose::Words::Saving::MarkdownEmptyParagraphExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_EmptyParagraphExportMode() const
```


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

* Enum [MarkdownEmptyParagraphExportMode](../../markdownemptyparagraphexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
