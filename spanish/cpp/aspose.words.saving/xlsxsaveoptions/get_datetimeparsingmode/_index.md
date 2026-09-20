---
title: "Método Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode"
linktitle: "get_DateTimeParsingMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode. Obtiene o establece el modo que especifica cómo se analiza el texto del documento para identificar valores de fecha y hora. El valor predeterminado es UseCurrentLocale en C++."
type: docs
weight: 3500
url: /es/cpp/aspose.words.saving/xlsxsaveoptions/get_datetimeparsingmode/
---
## XlsxSaveOptions::get_DateTimeParsingMode method


Obtiene o establece el modo que especifica cómo se analiza el texto del documento para identificar valores de fecha y hora. El valor predeterminado es [UseCurrentLocale](../../xlsxdatetimeparsingmode/).

```cpp
Aspose::Words::Saving::XlsxDateTimeParsingMode Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode() const
```


## Ejemplos



Muestra cómo especificar la autodetección del formato de fecha y hora.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Xlsx DateTime.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// Especifique el uso de la autodetección del formato de fecha y hora.
saveOptions->set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

## Ver también

* Enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
