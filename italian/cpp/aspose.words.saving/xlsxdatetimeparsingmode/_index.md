---
title: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum. Specifica come il testo del documento viene analizzato per identificare valori di data e ora in C++."
type: docs
weight: 86500
url: /it/cpp/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enum


Specifica come il testo del documento viene analizzato per identificare valori di data e ora.

```cpp
enum class XlsxDateTimeParsingMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| UseCurrentLocale | 0 | Il formato data/ora impostato per il thread corrente viene utilizzato per primo per analizzare i valori stringa. Se l'analisi fallisce, vengono provati altri formati data/ora comuni. |
| Auto | 1 | Il formato data/ora utilizzato in un documento viene determinato automaticamente. Questo può richiedere tempo aggiuntivo. |


## Esempi



Mostra come specificare l'autodetect del formato data/ora.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Xlsx DateTime.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// Specifica l'uso dell'autodetect del formato data/ora.
saveOptions->set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
