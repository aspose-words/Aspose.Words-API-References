---
title: "Método Aspose::Words::IHyphenationCallback::RequestDictionary. Notifica a la aplicación que el diccionario de guiones para el idioma especificado no se encontró y puede necesitar ser registrado. La implementación debe encontrar un diccionario y registrarlo usando los métodos RegisterDictionary(). Si el diccionario no está disponible para el idioma especificado, la implementación puede optar por no recibir más llamadas para el mismo idioma usando RegisterDictionary() con valor nulo en C++."
linktitle: "Método Aspose::Words::IHyphenationCallback::GetType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Cómo usar el método GetType de la clase Aspose::Words::IHyphenationCallback en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback::RequestDictionary method


Notifica a la aplicación que el diccionario de hifenación para el idioma especificado no se encontró y puede necesitar ser registrado. La implementación debe encontrar un diccionario y registrarlo usando los métodos [RegisterDictionary()](../). Si el diccionario no está disponible para el idioma especificado, la implementación puede optar por no recibir más llamadas para el mismo idioma usando [RegisterDictionary()](../) con el valor **null**.

```cpp
virtual void Aspose::Words::IHyphenationCallback::RequestDictionary(System::String language)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| idioma | System::String | Un nombre de idioma, p. ej. "en-US". Consulte la documentación de .NET para "culture name" y el RFC 4646 para obtener más detalles. |

## Ver también

* Interface [IHyphenationCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
