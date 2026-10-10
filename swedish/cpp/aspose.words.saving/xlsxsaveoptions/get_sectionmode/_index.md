---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode metod"
linktitle: "get_SectionMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode metod. Hämtar eller anger hur sektioner hanteras när man sparar till den resulterande XLSX-dokumentet. Standardvärdet är MultipleWorksheets i C++."
type: docs
weight: 4500
url: /sv/cpp/aspose.words.saving/xlsxsaveoptions/get_sectionmode/
---
## XlsxSaveOptions::get_SectionMode method


Hämtar eller anger hur sektioner hanteras när man sparar till det resulterande XLSX-dokumentet. Standardvärdet är [MultipleWorksheets](../../xlsxsectionmode/).

```cpp
Aspose::Words::Saving::XlsxSectionMode Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode() const
```


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

* Enum [XlsxSectionMode](../../xlsxsectionmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
