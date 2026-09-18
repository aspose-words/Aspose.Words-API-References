---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode Methode"
linktitle: "get_SectionMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode Methode. Gibt die Art und Weise zurück, wie Abschnitte beim Speichern in das Ausgabedokument XLSX behandelt werden, oder legt sie fest. Der Standardwert ist MultipleWorksheets in C++."
type: docs
weight: 4500
url: /de/cpp/aspose.words.saving/xlsxsaveoptions/get_sectionmode/
---
## XlsxSaveOptions::get_SectionMode method


Gibt die Art und Weise zurück, wie Abschnitte beim Speichern in das Ausgabedokument XLSX behandelt werden, oder legt sie fest. Der Standardwert ist [MultipleWorksheets](../../xlsxsectionmode/).

```cpp
Aspose::Words::Saving::XlsxSectionMode Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode() const
```


## Beispiele



Zeigt, wie ein Dokument als separate Arbeitsblätter gespeichert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Jeder Abschnitt eines Dokuments wird als separates Arbeitsblatt erstellt.
// Verwenden Sie 'SingleWorksheet', um das gesamte Dokument in einem Arbeitsblatt anzuzeigen.
auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_SectionMode(Aspose::Words::Saving::XlsxSectionMode::MultipleWorksheets);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

## Siehe auch

* Enum [XlsxSectionMode](../../xlsxsectionmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
