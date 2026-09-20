---
title: "Constructor Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions. Inicializa una nueva instancia de la clase FindReplaceOptions con la configuración predeterminada en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions::FindReplaceOptions() constructor


Inicializa una nueva instancia de la clase [FindReplaceOptions](../) con la configuración predeterminada.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions()
```


## Ejemplos



Muestra cómo reconocer y usar sustituciones dentro de los patrones de reemplazo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// El uso del modo heredado no admite muchas funciones avanzadas, por lo que debemos configurarlo en 'false'.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection) constructor


Inicializa una nueva instancia de la clase [FindReplaceOptions](../) con la dirección especificada.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dirección | Aspose::Words::Replacing::FindReplaceDirection | La dirección de la operación de buscar y reemplazar. |

## Ver también

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Inicializa una nueva instancia de la clase [FindReplaceOptions](../) con la dirección especificada y la devolución de llamada de reemplazo.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction, const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dirección | Aspose::Words::Replacing::FindReplaceDirection | La dirección de la operación de buscar y reemplazar. |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | La devolución de llamada a usar para reemplazar el texto encontrado. |

## Ver también

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Inicializa una nueva instancia de la clase [FindReplaceOptions](../) con la devolución de llamada de reemplazo especificada.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | La devolución de llamada a usar para reemplazar el texto encontrado. |

## Ver también

* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
