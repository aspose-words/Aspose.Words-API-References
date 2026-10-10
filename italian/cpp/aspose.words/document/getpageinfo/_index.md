---
title: "Aspose::Words::Document::GetPageInfo metodo"
linktitle: "GetPageInfo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::GetPageInfo metodo. Ottiene le dimensioni della pagina, l'orientamento e altre informazioni su una pagina che potrebbero essere utili per la stampa o il rendering in C++."
type: docs
weight: 62000
url: /it/cpp/aspose.words/document/getpageinfo/
---
## Document::GetPageInfo method


Ottiene le dimensioni della pagina, l'orientamento e altre informazioni su una pagina che potrebbero essere utili per la stampa o il rendering.

```cpp
System::SharedPtr<Aspose::Words::Rendering::PageInfo> Aspose::Words::Document::GetPageInfo(int32_t pageIndex)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageIndex | int32_t | L'indice della pagina basato su zero. |

## Esempi



Mostra come verificare se la pagina è a colori o meno.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Verifica che la prima pagina del documento non sia colorata.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Vedi anche

* Class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
