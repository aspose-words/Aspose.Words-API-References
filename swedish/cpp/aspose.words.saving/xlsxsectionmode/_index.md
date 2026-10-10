---
title: "Aspose::Words::Saving::XlsxSectionMode enum"
linktitle: "XlsxSectionMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XlsxSectionMode enum. Anger hur sektioner hanteras när ett dokument sparas i XLSX-formatet i C++."
type: docs
weight: 87000
url: /sv/cpp/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enum


Anger hur sektioner hanteras när ett dokument sparas i XLSX-format.

```cpp
enum class XlsxSectionMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| MultipleWorksheets | 0 | Anger att ett separat kalkylblad skapas för varje sektion i ett dokument. |
| SingleWorksheet | 1 | Anger att alla sektioner i ett dokument sparas på ett kalkylblad. |


## Exempel



Visar hur man sparar dokumentet som separata kalkylblad.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Varje avsnitt i ett dokument kommer att skapas som ett separat kalkylblad.
// Använd 'SingleWorksheet' för att visa hela dokumentet på ett kalkylblad.
auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_SectionMode(Aspose::Words::Saving::XlsxSectionMode::MultipleWorksheets);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
