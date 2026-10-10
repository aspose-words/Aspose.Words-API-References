---
title: "Clase Aspose::Words::Hyphenation"
linktitle: "Separación silábica"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Hyphenation. Proporciona métodos para trabajar con diccionarios de separación silábica. Estos diccionarios indican dónde pueden separarse palabras de un idioma específico. Para obtener más información, visita el artículo de documentación en C++."
type: docs
weight: 33000
url: /es/cpp/aspose.words/hyphenation/
---
## Hyphenation class


Proporciona métodos para trabajar con diccionarios de guionización. Estos diccionarios indican dónde se pueden dividir en sílabas las palabras de un idioma específico. Para obtener más información, visite el artículo de documentación [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class Hyphenation
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [get_Callback](./get_callback/)() | Obtiene la interfaz de devolución de llamada utilizada para solicitar diccionarios cuando se construye el diseño de página del documento. Esto permite cargar los diccionarios de forma diferida, lo que puede ser útil al procesar documentos en varios idiomas. |
| static [get_WarningCallback](./get_warningcallback/)() | Se llama durante la carga de patrones de separación silábica, cuando se detecta un problema que podría provocar una pérdida de fidelidad de formato. |
| [Hyphenation](./hyphenation/)() |  |
| static [IsDictionaryRegistered](./isdictionaryregistered/)(const System::String\&) | Devuelve **false** si para el idioma especificado no hay ningún diccionario registrado o si el registrado es un diccionario Null, **true** en caso contrario. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) | Registra y carga un diccionario de separación silábica para el idioma especificado desde un flujo. Lanza una excepción si el diccionario no se puede leer o tiene un formato inválido. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::String\&) | Registra y carga un diccionario de separación silábica para el idioma especificado desde un archivo. Lanza una excepción si el diccionario no se puede leer o tiene un formato inválido. Este método también puede usarse para registrar un diccionario Null y evitar que [Callback](./get_callback/) sea llamado repetidamente para el mismo idioma. |
| static [RegisterDictionary](./registerdictionary/)(System::String, std::basic_istream\<CharType, Traits\>\&) |  |
| static [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::IHyphenationCallback\>\&) | Establece la interfaz de devolución de llamada utilizada para solicitar diccionarios cuando se construye el diseño de página del documento. Esto permite cargar los diccionarios de forma diferida, lo que puede ser útil al procesar documentos en varios idiomas. |
| static [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Se llama durante la carga de patrones de separación silábica, cuando se detecta un problema que podría provocar una pérdida de fidelidad de formato. |
| static [UnregisterDictionary](./unregisterdictionary/)(const System::String\&) | Anula el registro de un diccionario de separación silábica para el idioma especificado. Esto es diferente de registrar un diccionario Null. Anular el registro de un diccionario habilita la devolución de llamada para el idioma especificado. |
## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
