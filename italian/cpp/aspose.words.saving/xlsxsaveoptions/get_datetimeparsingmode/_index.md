---
title: "Metodo Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode"
linktitle: "get_DateTimeParsingMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode. Ottiene o imposta la modalità che specifica come il testo del documento viene analizzato per identificare valori di data e ora. Il valore predefinito è UseCurrentLocale in C++."
type: docs
weight: 3500
url: /it/cpp/aspose.words.saving/xlsxsaveoptions/get_datetimeparsingmode/
---
## XlsxSaveOptions::get_DateTimeParsingMode method


Ottiene o imposta la modalità che specifica come il testo del documento viene analizzato per identificare valori di data e ora. Il valore predefinito è [UseCurrentLocale](../../xlsxdatetimeparsingmode/).

```cpp
Aspose::Words::Saving::XlsxDateTimeParsingMode Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode() const
```


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

* Enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
