---
title: "Metodo Aspose::Words::Document::RemoveMacros"
linktitle: "RemoveMacros"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::RemoveMacros. Rimuove tutte le macro (il progetto VBA) così come le barre degli strumenti e le personalizzazioni dei comandi dal documento in C++."
type: docs
weight: 69000
url: /it/cpp/aspose.words/document/removemacros/
---
## Document::RemoveMacros method


Rimuove tutte le macro (il progetto VBA) così come le barre degli strumenti e le personalizzazioni dei comandi dal documento.

```cpp
void Aspose::Words::Document::RemoveMacros()
```

## Note


Rimuovendo tutte le macro da un documento è possibile garantire che il documento non contenga virus macro.

## Esempi



Mostra come rimuovere tutte le macro da un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");

ASSERT_TRUE(doc->get_HasMacros());
ASSERT_EQ(u"Project", doc->get_VbaProject()->get_Name());

// Rimuove il progetto VBA del documento, insieme a tutte le sue macro.
doc->RemoveMacros();

ASSERT_FALSE(doc->get_HasMacros());
ASSERT_TRUE(System::TestTools::IsNull(doc->get_VbaProject()));
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
