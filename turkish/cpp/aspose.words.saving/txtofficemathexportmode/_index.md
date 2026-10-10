---
title: "Aspose::Words::Saving::TxtOfficeMathExportMode enum"
linktitle: "TxtOfficeMathExportMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtOfficeMathExportMode enum. Aspose.Words'ın OfficeMath'i C++'ta Metin olarak nasıl dışa aktardığını belirtir."
type: docs
weight: 86250
url: /tr/cpp/aspose.words.saving/txtofficemathexportmode/
---
## TxtOfficeMathExportMode enum


Aspose.Words'ın OfficeMath'i [Metin](../../aspose.words/saveformat/) olarak nasıl dışa aktardığını belirtir.

```cpp
enum class TxtOfficeMathExportMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Metin | 0 | OfficeMath'i düz metin olarak dışa aktar. |
| Latex | 3 | OfficeMath'i LaTeX olarak dışa aktar. |


## Örnekler



OfficeMath nesnesini TXT içinde LaTeX olarak nasıl dışa aktarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
