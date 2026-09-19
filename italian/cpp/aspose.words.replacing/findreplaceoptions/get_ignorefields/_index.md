---
title: "Metodo Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields"
linktitle: "get_IgnoreFields"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields. Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno dei campi. Il valore predefinito è false in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefields/
---
## FindReplaceOptions::get_IgnoreFields method


Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno dei campi. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields() const
```

## Note


Questa opzione influisce sull'intero campo (tutti i nodi tra [FieldStart](../../../aspose.words/nodetype/) e [FieldEnd](../../../aspose.words/nodetype/)).

Per ignorare solo i codici di campo, utilizza l'opzione corrispondente [IgnoreFieldCodes](../get_ignorefieldcodes/).

## Esempi



Mostra come ignorare il testo all'interno dei campi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertField(u"QUOTE", u"Hello again!");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta il flag "IgnoreFields" su "true" per ottenere la ricerca e sostituzione
// operazione per ignorare il testo all'interno dei campi.
// Imposta il flag "IgnoreFields" su "false" per ottenere la ricerca e sostituzione
// operazione per cercare anche il testo all'interno dei campi.
options->set_IgnoreFields(ignoreTextInsideFields);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideFields ? System::String(u"Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015") : System::String(u"Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015"), doc->GetText().Trim());
```

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
