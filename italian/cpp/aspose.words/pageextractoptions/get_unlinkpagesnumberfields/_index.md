---
title: "metodo Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields"
linktitle: "get_UnlinkPagesNumberFields"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields. Specifica se i campi NUMPAGES nel documento risultante saranno sostituiti con i loro valori effettivi. Il valore predefinito è true in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/pageextractoptions/get_unlinkpagesnumberfields/
---
## PageExtractOptions::get_UnlinkPagesNumberFields method


Specifica se i campi NUMPAGES nel documento risultante saranno sostituiti con i loro valori effettivi. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields() const
```


## Esempi



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

* Class [PageExtractOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
