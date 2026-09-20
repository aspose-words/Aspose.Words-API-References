---
title: "Método Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields"
linktitle: "get_IgnoreFields"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields. Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de los campos. El valor predeterminado es false en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefields/
---
## FindReplaceOptions::get_IgnoreFields method


Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de campos. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields() const
```

## Observaciones


Esta opción afecta a todo el campo (todos los nodos entre [FieldStart](../../../aspose.words/nodetype/) y [FieldEnd](../../../aspose.words/nodetype/)).

Para ignorar solo los códigos de campo, utilice la opción correspondiente [IgnoreFieldCodes](../get_ignorefieldcodes/).

## Ejemplos



Muestra cómo ignorar texto dentro de los campos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertField(u"QUOTE", u"Hello again!");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Establezca la bandera "IgnoreFields" a "true" para obtener la operación de buscar y reemplazar
// operación para ignorar texto dentro de los campos.
// Establezca la bandera "IgnoreFields" a "false" para obtener la operación de buscar y reemplazar
// operación para también buscar texto dentro de los campos.
options->set_IgnoreFields(ignoreTextInsideFields);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideFields ? System::String(u"Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015") : System::String(u"Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015"), doc->GetText().Trim());
```

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
