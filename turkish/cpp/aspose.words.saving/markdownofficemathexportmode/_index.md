---
title: "Aspose::Words::Saving::MarkdownOfficeMathExportMode enum"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownOfficeMathExportMode enum. Aspose.Words'un OfficeMath'i C++'da Markdown formatına nasıl dışa aktardığını belirtir."
type: docs
weight: 68500
url: /tr/cpp/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enum


Aspose.Words'in OfficeMath'i Markdown formatına nasıl dışa aktardığını belirtir.

```cpp
enum class MarkdownOfficeMathExportMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Metin | 0 | OfficeMath'i düz metin olarak dışa aktar. |
| Image | 1 | OfficeMath'i görüntü olarak dışa aktar. |
| MathML | 2 | OfficeMath'i MathML olarak dışa aktar. |
| Latex | 3 | OfficeMath'i LaTeX olarak dışa aktar. |
| MarkItDown | 4 | OfficeMath'i MarkItDown ile uyumlu LaTeX olarak dışa aktar. |


## Örnekler



OfficeMath'in belgeye nasıl yazılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Image);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```


OfficeMath nesnesinin Latex olarak nasıl dışa aktarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
```


OfficeMath nesnesinin MarkItDown olarak nasıl dışa aktarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::MarkItDown);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
