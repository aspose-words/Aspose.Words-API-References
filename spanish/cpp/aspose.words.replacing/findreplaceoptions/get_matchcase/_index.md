---
title: "Método Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase"
linktitle: "get_MatchCase"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase. True indica comparación sensible a mayúsculas, false indica comparación insensible a mayúsculas en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_matchcase/
---
## FindReplaceOptions::get_MatchCase method


True indica comparación sensible a mayúsculas y minúsculas, false indica comparación insensible a mayúsculas y minúsculas.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase() const
```


## Ejemplos



Muestra cómo alternar la sensibilidad a mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Establezca la bandera "MatchCase" a "true" para aplicar sensibilidad a mayúsculas y minúsculas al buscar cadenas para reemplazar.
// Establezca la bandera "MatchCase" a "false" para ignorar mayúsculas y minúsculas al buscar texto para reemplazar.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
