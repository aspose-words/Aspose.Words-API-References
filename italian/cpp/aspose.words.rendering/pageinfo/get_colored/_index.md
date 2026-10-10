---
title: "Metodo get_Colored di Aspose::Words::Rendering::PageInfo"
linktitle: "get_Colored"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_Colored di Aspose::Words::Rendering::PageInfo. Restituisce true se la pagina contiene contenuto a colori in C++."
type: docs
weight: 1500
url: /it/cpp/aspose.words.rendering/pageinfo/get_colored/
---
## PageInfo::get_Colored method


Restituisce **true** se la pagina contiene contenuto a colori.

```cpp
bool Aspose::Words::Rendering::PageInfo::get_Colored()
```


## Esempi



Mostra come verificare se la pagina è a colori o meno.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Verifica che la prima pagina del documento non sia colorata.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Vedi anche

* Class [PageInfo](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
