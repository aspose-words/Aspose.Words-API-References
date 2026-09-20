---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes método"
linktitle: "get_IgnoreFieldCodes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes método. Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de los códigos de campo. El valor predeterminado es false en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefieldcodes/
---
## FindReplaceOptions::get_IgnoreFieldCodes method


Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de códigos de campo. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes() const
```

## Observaciones


Esta opción afecta solo a los códigos de campo (no ignora los nodos entre [FieldSeparator](../../../aspose.words/nodetype/) y [FieldEnd](../../../aspose.words/nodetype/)).

Para ignorar todo el campo, utilice la opción correspondiente [IgnoreFields](../get_ignorefields/).

## Ejemplos



Muestra cómo ignorar el texto dentro de los códigos de campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u"INCLUDETEXT", u"Test IT!");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFieldCodes(ignoreFieldCodes);

// Reemplazar 'T' en el documento ignorando el texto dentro del código de campo o no.
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"T"), u"*", options);
std::cout << doc->GetText() << std::endl;

ASSERT_EQ(ignoreFieldCodes ? System::String(u"\u0013INCLUDETEXT\u0014*est I*!\u0015") : System::String(u"\u0013INCLUDE*EX*\u0014*est I*!\u0015"), doc->GetText().Trim());
```

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
