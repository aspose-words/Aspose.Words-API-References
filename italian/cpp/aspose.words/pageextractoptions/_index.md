---
title: "Classe Aspose::Words::PageExtractOptions"
linktitle: "PageExtractOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::PageExtractOptions. Consente di specificare le opzioni per l'estrazione delle pagine del documento in C++."
type: docs
weight: 45500
url: /it/cpp/aspose.words/pageextractoptions/
---
## PageExtractOptions class


Consente di specificare le opzioni per l'estrazione delle pagine del documento.

```cpp
class PageExtractOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/)() const | Specifica se i campi NUMPAGES nel documento risultante saranno sostituiti con i loro valori effettivi. Il valore predefinito è **true**. |
| [get_UpdatePageStartingNumber](./get_updatepagestartingnumber/)() const | Specifica se il numero della pagina iniziale nel documento risultante deve essere aggiornato. Il valore predefinito è **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageExtractOptions](./pageextractoptions/)() |  |
| [set_UnlinkPagesNumberFields](./set_unlinkpagesnumberfields/)(bool) | Setter per [Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/). |
| [set_UpdatePageStartingNumber](./set_updatepagestartingnumber/)(bool) | Setter per [Aspose::Words::PageExtractOptions::get_UpdatePageStartingNumber](./get_updatepagestartingnumber/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
