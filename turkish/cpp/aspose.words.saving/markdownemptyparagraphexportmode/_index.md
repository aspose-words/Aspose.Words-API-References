---
title: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode enum"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode enum. Aspose.Words'un C++'ta boş paragrafları Markdown'a nasıl dışa aktardığını belirtir."
type: docs
weight: 66250
url: /tr/cpp/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enum


Aspose.Words'in boş paragrafları Markdown formatına nasıl dışa aktardığını belirtir.

```cpp
enum class MarkdownEmptyParagraphExportMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| EmptyLine | 0 | Boş satırlar olarak dışa aktar. |
| MarkdownHardLineBreak | 1 | Markdown HardLineBreak karakteri '\' olarak dışa aktar. |
| None | 2 | Boş paragrafları dışa aktarma. |


## Örnekler



Boş paragrafların nasıl dışa aktarılacağını gösterir.
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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
