---
title: "Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode metodu"
linktitle: "get_OfficeMathExportMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode metodu. OfficeMath'in çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer C++'ta Text'tir."
type: docs
weight: 5500
url: /tr/cpp/aspose.words.saving/txtsaveoptions/get_officemathexportmode/
---
## TxtSaveOptions::get_OfficeMathExportMode method


OfficeMath'in çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer [Text](../../txtofficemathexportmode/)dır.

```cpp
Aspose::Words::Saving::TxtOfficeMathExportMode Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode() const
```


## Örnekler



OfficeMath nesnesini TXT içinde LaTeX olarak nasıl dışa aktarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Ayrıca Bakınız

* Enum [TxtOfficeMathExportMode](../../txtofficemathexportmode/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
