---
title: "Aspose::Words::Saving::TxtOfficeMathExportMode enum"
linktitle: "TxtOfficeMathExportMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::TxtOfficeMathExportMode enum. Gibt an, wie Aspose.Words OfficeMath in Text in C++ exportiert."
type: docs
weight: 86250
url: /de/cpp/aspose.words.saving/txtofficemathexportmode/
---
## TxtOfficeMathExportMode enum


Gibt an, wie Aspose.Words OfficeMath nach [Text](../../aspose.words/saveformat/) exportiert.

```cpp
enum class TxtOfficeMathExportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Text | 0 | Exportiere OfficeMath als Klartext. |
| Latex | 3 | Exportiere OfficeMath als LaTeX. |


## Beispiele



Zeigt, wie das OfficeMath‑Objekt als LaTeX in TXT exportiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
