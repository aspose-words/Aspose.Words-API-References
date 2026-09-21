---
title: "Aspose::Words::Saving::TxtOfficeMathExportMode enum"
linktitle: "TxtOfficeMathExportMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::TxtOfficeMathExportMode enum. Anger hur Aspose.Words exporterar OfficeMath till Text i C++."
type: docs
weight: 86250
url: /sv/cpp/aspose.words.saving/txtofficemathexportmode/
---
## TxtOfficeMathExportMode enum


Anger hur Aspose.Words exporterar OfficeMath till [Text](../../aspose.words/saveformat/).

```cpp
enum class TxtOfficeMathExportMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Text | 0 | Exportera OfficeMath som vanlig text. |
| Latex | 3 | Exportera OfficeMath som LaTeX. |


## Exempel



Visar hur man exporterar OfficeMath-objekt som Latex i TXT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
