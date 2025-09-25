---
title: Aspose::Words::Saving::MarkdownOfficeMathExportMode enum
linktitle: MarkdownOfficeMathExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownOfficeMathExportMode enum. Specifies how Aspose.Words exports OfficeMath to Markdown in C++.'
type: docs
weight: 68500
url: /cpp/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enum


Specifies how Aspose.Words exports OfficeMath to Markdown.

```cpp
enum class MarkdownOfficeMathExportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Text | 0 | Export OfficeMath as plain text. |
| Image | 1 | Export OfficeMath as image. |
| MathML | 2 | Export OfficeMath as MathML. |
| Latex | 3 | Export OfficeMath as LaTeX. |


## Examples



Shows how OfficeMath will be written to the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Image);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```


Shows how to export OfficeMath object as Latex. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
