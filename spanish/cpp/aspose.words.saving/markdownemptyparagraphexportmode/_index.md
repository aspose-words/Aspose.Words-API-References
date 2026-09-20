---
title: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode enum"
linktitle: "MarkdownEmptyParagraphExportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MarkdownEmptyParagraphExportMode enum. Especifica cómo Aspose.Words exporta párrafos vacíos a Markdown en C++."
type: docs
weight: 66250
url: /es/cpp/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enum


Especifica cómo Aspose.Words exporta párrafos vacíos a Markdown.

```cpp
enum class MarkdownEmptyParagraphExportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| EmptyLine | 0 | Exportar como líneas vacías. |
| MarkdownHardLineBreak | 1 | Exportar como carácter de salto de línea duro de Markdown '\\'. |
| None | 2 | No exportar párrafos vacíos. |


## Ejemplos



Muestra cómo exportar párrafos vacíos.
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

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
