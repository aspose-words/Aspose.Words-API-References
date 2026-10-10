---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode yöntemi"
linktitle: "get_OfficeMathExportMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode yöntemi. OfficeMath'in çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer C++'da Text'tir."
type: docs
weight: 6500
url: /tr/cpp/aspose.words.saving/markdownsaveoptions/get_officemathexportmode/
---
## MarkdownSaveOptions::get_OfficeMathExportMode method


OfficeMath'in çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer [Text](../../markdownofficemathexportmode/).

```cpp
Aspose::Words::Saving::MarkdownOfficeMathExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode() const
```


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

* Enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
