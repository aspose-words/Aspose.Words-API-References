---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode Methode"
linktitle: "get_DateTimeParsingMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode Methode. Gibt den Modus zurück, der festlegt, wie Dokumententext geparst wird, um Datums- und Zeitwerte zu identifizieren, oder legt ihn fest. Der Standardwert ist UseCurrentLocale in C++."
type: docs
weight: 3500
url: /de/cpp/aspose.words.saving/xlsxsaveoptions/get_datetimeparsingmode/
---
## XlsxSaveOptions::get_DateTimeParsingMode method


Gibt den Modus zurück, der festlegt, wie Dokumententext geparst wird, um Datums- und Zeitwerte zu identifizieren, oder legt ihn fest. Der Standardwert ist [UseCurrentLocale](../../xlsxdatetimeparsingmode/).

```cpp
Aspose::Words::Saving::XlsxDateTimeParsingMode Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode() const
```


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

* Enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
