---
title: "Método Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions"
linktitle: "get_UseSubstitutions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions. Obtiene o establece un valor booleano que indica si se deben reconocer y usar sustituciones dentro de los patrones de reemplazo. El valor predeterminado es false en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_usesubstitutions/
---
## FindReplaceOptions::get_UseSubstitutions method


Obtiene o establece un valor booleano que indica si se deben reconocer y usar sustituciones dentro de los patrones de reemplazo. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions() const
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


Muestra cómo reemplazar el texto con sustituciones.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"John sold a car to Paul.");
builder->Writeln(u"Jane sold a house to Joe.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Establezca la propiedad "UseSubstitutions" en "true" para obtener
// la operación de buscar y reemplazar para reconocer los elementos de sustitución.
// Establezca la propiedad "UseSubstitutions" en "false" para ignorar los elementos de sustitución.
options->set_UseSubstitutions(useSubstitutions);

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc->get_Range()->Replace(regex, u"$3 bought a $2 from $1", options);

ASSERT_EQ(useSubstitutions ? System::String(u"Paul bought a car from John.\rJoe bought a house from Jane.") : System::String(u"$3 bought a $2 from $1.\r$3 bought a $2 from $1."), doc->GetText().Trim());
```

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
