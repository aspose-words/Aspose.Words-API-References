---
title: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum. Anger hur dokumenttext parsas för att identifiera datum- och tidsvärden i C++."
type: docs
weight: 86500
url: /sv/cpp/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enum


Anger hur dokumenttexten analyseras för att identifiera datum- och tidsvärden.

```cpp
enum class XlsxDateTimeParsingMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| UseCurrentLocale | 0 | Det datum- och tidsformat som är inställt för den aktuella tråden används först för att tolka strängvärden. Om tolkningen misslyckas provas andra vanliga datum- och tidsformat. |
| Auto | 1 | Datum- och tidsformatet som används i ett dokument bestäms automatiskt. Detta kan ta extra tid. |


## Exempel



Visar hur man specificerar automatisk upptäckt av datum- och tidsformatet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Xlsx DateTime.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// Ange att använda automatisk upptäckt av datum- och tidsformat.
saveOptions->set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
