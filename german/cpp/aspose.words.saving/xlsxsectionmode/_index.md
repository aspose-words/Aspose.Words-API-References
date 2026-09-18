---
title: "Aspose::Words::Saving::XlsxSectionMode enum"
linktitle: "XlsxSectionMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XlsxSectionMode enum. Gibt an, wie Abschnitte beim Speichern eines Dokuments im XLSX‑Format in C++ behandelt werden."
type: docs
weight: 87000
url: /de/cpp/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enum


Gibt an, wie Abschnitte beim Speichern eines Dokuments im XLSX-Format behandelt werden.

```cpp
enum class XlsxSectionMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| MultipleWorksheets | 0 | Gibt an, dass für jeden Abschnitt eines Dokuments ein separates Arbeitsblatt erstellt wird. |
| SingleWorksheet | 1 | Gibt an, dass alle Abschnitte eines Dokuments in einem Arbeitsblatt gespeichert werden. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
