---
title: "interfaz Aspose::Words::IHyphenationCallback"
linktitle: "IHyphenationCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "interfaz Aspose::Words::IHyphenationCallback. Implementada por clases que pueden registrar diccionarios de hifenación en C++."
type: docs
weight: 78000
url: /es/cpp/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface


Implementado por clases que pueden registrar diccionarios de guiones.

```cpp
class IHyphenationCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RequestDictionary](./requestdictionary/)(System::String) | Notifica a la aplicación que el diccionario de hifenación para el idioma especificado no se encontró y puede necesitar ser registrado. La implementación debe encontrar un diccionario y registrarlo usando los métodos [RegisterDictionary()](../). Si el diccionario no está disponible para el idioma especificado, la implementación puede optar por no recibir más llamadas para el mismo idioma usando [RegisterDictionary()](../) con el valor **null**. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
