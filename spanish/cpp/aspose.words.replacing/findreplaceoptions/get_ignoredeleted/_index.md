---
title: "Método Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted"
linktitle: "get_IgnoreDeleted"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted. Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de revisiones de eliminación. El valor predeterminado es false en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_ignoredeleted/
---
## FindReplaceOptions::get_IgnoreDeleted method


Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de revisiones de eliminación. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted() const
```


## Ejemplos



Muestra cómo incluir o ignorar texto dentro de revisiones de eliminación durante una operación de buscar y reemplazar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Comience a rastrear revisiones y elimine el segundo párrafo, lo que creará una revisión de eliminación.
// Ese párrafo permanecerá en el documento hasta que aceptemos la revisión de eliminación.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->Remove();
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsDeleteRevision());

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Establezca la bandera "IgnoreDeleted" a "true" para obtener la operación de buscar y reemplazar
// operación para ignorar párrafos que son revisiones de eliminación.
// Establezca la bandera "IgnoreDeleted" a "false" para obtener la operación de buscar y reemplazar
// operación para también buscar texto dentro de revisiones de eliminación.
options->set_IgnoreDeleted(ignoreTextInsideDeleteRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideDeleteRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
