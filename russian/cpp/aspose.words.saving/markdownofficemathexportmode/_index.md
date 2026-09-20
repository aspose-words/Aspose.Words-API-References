---
title: "Aspose::Words::Saving::MarkdownOfficeMathExportMode enum"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::MarkdownOfficeMathExportMode enum. Указывает, как Aspose.Words экспортирует OfficeMath в Markdown в C++."
type: docs
weight: 68500
url: /ru/cpp/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enum


Указывает, как Aspose.Words экспортирует OfficeMath в Markdown.

```cpp
enum class MarkdownOfficeMathExportMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Text | 0 | Экспортировать OfficeMath как простой текст. |
| Image | 1 | Экспортировать OfficeMath как изображение. |
| MathML | 2 | Экспортировать OfficeMath как MathML. |
| Latex | 3 | Экспортировать OfficeMath как LaTeX. |
| MarkItDown | 4 | Экспортировать OfficeMath как LaTeX, совместимый с MarkItDown. |


## Примеры



Показывает, как OfficeMath будет записан в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Image);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```


Показывает, как экспортировать объект OfficeMath как LaTeX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
```


Показывает, как экспортировать объект OfficeMath как MarkItDown.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::MarkItDown);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
