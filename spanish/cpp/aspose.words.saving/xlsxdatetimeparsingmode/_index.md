---
title: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum. Especifica cómo se analiza el texto del documento para identificar valores de fecha y hora en C++."
type: docs
weight: 86500
url: /es/cpp/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enum


Especifica cómo se analiza el texto del documento para identificar valores de fecha y hora.

```cpp
enum class XlsxDateTimeParsingMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| UseCurrentLocale | 0 | El formato de fecha y hora establecido para el hilo actual se usa primero para analizar valores de cadena. Si el análisis falla, se prueban otros formatos de fecha y hora comunes. |
| Auto | 1 | El formato de fecha y hora utilizado en un documento se determina automáticamente. Esto puede requerir tiempo adicional. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
