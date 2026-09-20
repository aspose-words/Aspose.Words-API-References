---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted método"
linktitle: "get_IgnoreInserted"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted método. Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de revisiones de inserción. El valor predeterminado es false en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreinserted/
---
## FindReplaceOptions::get_IgnoreInserted method


Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de revisiones de inserción. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted() const
```


## Ejemplos



Muestra cómo incluir o ignorar texto dentro de revisiones de inserción durante una operación de buscar y reemplazar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

// Comience a rastrear revisiones e inserte un párrafo. Ese párrafo será una revisión de inserción.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"Hello again!");
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsInsertRevision());

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Establezca la bandera "IgnoreInserted" a "true" para obtener la operación de buscar y reemplazar
// para que ignore los párrafos que son revisiones de inserción.
// Establezca la bandera "IgnoreInserted" a "false" para obtener la operación de buscar y reemplazar
// para también buscar texto dentro de revisiones de inserción.
options->set_IgnoreInserted(ignoreTextInsideInsertRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideInsertRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
