---
title: "Metodo Aspose::Words::Document::ExtractPages"
linktitle: "ExtractPages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::ExtractPages. Restituisce l'oggetto Document che rappresenta l'intervallo specificato di pagine in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/document/extractpages/
---
## Document::ExtractPages(int32_t, int32_t) method


Restituisce l'oggetto [Document](../) che rappresenta l'intervallo specificato di pagine.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | L'indice basato su zero della prima pagina da estrarre. |
| count | int32_t | Numero di pagine da estrarre. |

## Esempi



Mostra come ottenere l'intervallo specificato di pagine dal documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(get_ArtifactsDir() + u"Document.ExtractPages.docx");
```


Mostra come reimpostare la numerazione delle pagine iniziale e salvare il campo NUMPAGE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Page fields.docx");

// Comportamento predefinito:
// La numerazione delle pagine estratta è la stessa del documento originale, come se avessimo selezionato "Stampa 2 pagine" in MS Word.
// La pagina iniziale sarà impostata a 2 e il campo che indica il numero di pagine sarà rimosso
// e sostituito con un valore costante pari al numero di pagine.
System::SharedPtr<Aspose::Words::Document> extractedDoc1 = doc->ExtractPages(1, 1);
extractedDoc1->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Default.docx");

// Comportamento modificato:
// La numerazione delle pagine estratta viene reimpostata e ne inizia una nuova,
// come se avessimo copiato il contenuto della seconda pagina e incollato in un nuovo documento.
// La pagina iniziale sarà impostata a 1 e il campo che indica il numero di pagine rimarrà invariato
// e mostrerà il numero corrente di pagine.
auto extractOptions = System::MakeObject<Aspose::Words::PageExtractOptions>();
extractOptions->set_UpdatePageStartingNumber(false);
extractOptions->set_UnlinkPagesNumberFields(false);
System::SharedPtr<Aspose::Words::Document> extractedDoc2 = doc->ExtractPages(1, 1, extractOptions);
extractedDoc2->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Options.docx");
```

## Vedi anche

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::ExtractPages(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) method


Restituisce l'oggetto [Document](../) che rappresenta l'intervallo di pagine specificato e le opzioni di estrazione della pagina fornite.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count, const System::SharedPtr<Aspose::Words::PageExtractOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | L'indice basato su zero della prima pagina da estrarre. |
| count | int32_t | Numero di pagine da estrarre. |
| opzioni | const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\& | Fornisce opzioni per gestire il processo di estrazione delle pagine. |

## Vedi anche

* Class [Document](../)
* Class [PageExtractOptions](../../pageextractoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
