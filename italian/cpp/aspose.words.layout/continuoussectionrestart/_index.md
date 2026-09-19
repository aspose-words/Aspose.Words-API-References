---
title: "Aspose::Words::Layout::ContinuousSectionRestart enum"
linktitle: "ContinuousSectionRestart"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::ContinuousSectionRestart enum. Rappresenta diversi comportamenti durante il calcolo dei numeri di pagina in una sezione continua che riavvia la numerazione delle pagine in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enum


Rappresenta comportamenti diversi durante il calcolo dei numeri di pagina in una sezione continua che ripristina la numerazione delle pagine.

```cpp
enum class ContinuousSectionRestart
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Sempre | 0 | La numerazione delle pagine si riavvia sempre, indipendentemente dal flusso del contenuto. |
| FromNewPageOnly | 1 | La numerazione delle pagine si riavvia solo se non c'è altro contenuto prima della sezione nella pagina in cui la sezione inizia. |


## Esempi



Mostra come controllare la numerazione delle pagine in una sezione continua.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Continuous section page numbering.docx");

// Per impostazione predefinita il comportamento di Aspose.Words corrisponde a Microsoft Word 2019.
// Se hai bisogno del vecchio comportamento di Aspose.Words, come in Microsoft Word 2016, usa 'ContinuousSectionRestart.FromNewPageOnly'.
// La numerazione delle pagine si riavvia solo se non c'è altro contenuto prima della sezione nella pagina in cui la sezione inizia,
// perché in tal caso la numerazione verrà ripristinata a 2 dalla seconda pagina.
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(Aspose::Words::Layout::ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```

## Vedi anche

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
