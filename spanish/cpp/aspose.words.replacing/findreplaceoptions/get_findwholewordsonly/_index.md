---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly método"
linktitle: "get_FindWholeWordsOnly"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly método. True indica que oldValue debe ser una palabra independiente en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_findwholewordsonly/
---
## FindReplaceOptions::get_FindWholeWordsOnly method


True indica que oldValue debe ser una palabra independiente.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly() const
```


## Ejemplos



Muestra cómo alternar operaciones de buscar y reemplazar que solo afectan palabras independientes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Establezca la bandera "FindWholeWordsOnly" a "true" para reemplazar el texto encontrado si no forma parte de otra palabra.
// Establezca la bandera "FindWholeWordsOnly" a "false" para reemplazar todo el texto sin importar su contexto.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
