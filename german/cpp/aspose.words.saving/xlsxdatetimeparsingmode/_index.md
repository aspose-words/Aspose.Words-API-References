---
title: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XlsxDateTimeParsingMode‑Enum. Gibt an, wie Dokumenttext analysiert wird, um Datums‑ und Zeitwerte in C++ zu identifizieren."
type: docs
weight: 86500
url: /de/cpp/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enum


Gibt an, wie Dokumenttext analysiert wird, um Datums‑ und Zeitwerte zu erkennen.

```cpp
enum class XlsxDateTimeParsingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| UseCurrentLocale | 0 | Das für den aktuellen Thread festgelegte Datums‑Zeit‑Format wird zuerst verwendet, um Zeichenkettenwerte zu analysieren. Wenn die Analyse fehlschlägt, werden weitere gängige Datums‑Zeit‑Formate ausprobiert. |
| Auto | 1 | Das in einem Dokument verwendete Datums‑Zeit‑Format wird automatisch ermittelt. Dies kann zusätzlichen Zeitaufwand bedeuten. |


## Beispiele



Zeigt, wie die automatische Erkennung des Datums‑Zeit‑Formats angegeben wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Xlsx DateTime.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// Geben Sie die Verwendung der automatischen Erkennung des Datums‑Zeit‑Formats an.
saveOptions->set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
