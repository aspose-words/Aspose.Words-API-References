---
title: "Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode-Methode"
linktitle: "get_OfficeMathExportMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode-Methode. Gibt an, wie OfficeMath in die Ausgabedatei geschrieben wird. Der Standardwert ist Text in C++."
type: docs
weight: 5500
url: /de/cpp/aspose.words.saving/txtsaveoptions/get_officemathexportmode/
---
## TxtSaveOptions::get_OfficeMathExportMode method


Gibt an, wie OfficeMath in die Ausgabedatei geschrieben wird. Der Standardwert ist [Text](../../txtofficemathexportmode/).

```cpp
Aspose::Words::Saving::TxtOfficeMathExportMode Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode() const
```


## Beispiele



Zeigt, wie das OfficeMath‑Objekt als LaTeX in TXT exportiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Siehe auch

* Enum [TxtOfficeMathExportMode](../../txtofficemathexportmode/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
