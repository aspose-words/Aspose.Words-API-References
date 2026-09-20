---
title: "Método get_LegacyMode de Aspose::Words::Replacing::FindReplaceOptions"
linktitle: "get_LegacyMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_LegacyMode de Aspose::Words::Replacing::FindReplaceOptions. Obtiene o establece un valor booleano que indica que se utiliza el algoritmo antiguo de búsqueda/reemplazo en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_legacymode/
---
## FindReplaceOptions::get_LegacyMode method


Obtiene o establece un valor booleano que indica que se utiliza el algoritmo antiguo de búsqueda/reemplazo.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode() const
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
