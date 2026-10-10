---
title: "Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode‑metod"
linktitle: "get_OfficeMathExportMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode‑metod. Anger hur OfficeMath kommer att skrivas till utdatafilen. Standardvärdet är Text i C++."
type: docs
weight: 5500
url: /sv/cpp/aspose.words.saving/txtsaveoptions/get_officemathexportmode/
---
## TxtSaveOptions::get_OfficeMathExportMode method


Anger hur OfficeMath kommer att skrivas till utdatafilen. Standardvärdet är [Text](../../txtofficemathexportmode/).

```cpp
Aspose::Words::Saving::TxtOfficeMathExportMode Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode() const
```


## Exempel



Visar hur man exporterar OfficeMath-objekt som Latex i TXT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Se även

* Enum [TxtOfficeMathExportMode](../../txtofficemathexportmode/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
