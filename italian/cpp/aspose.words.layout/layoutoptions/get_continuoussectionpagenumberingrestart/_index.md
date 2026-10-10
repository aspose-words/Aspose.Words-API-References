---
title: "Metodo Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart"
linktitle: "get_ContinuousSectionPageNumberingRestart"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart. Ottiene o imposta la modalità di comportamento per il calcolo dei numeri di pagina quando una sezione continua riavvia la numerazione delle pagine in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.layout/layoutoptions/get_continuoussectionpagenumberingrestart/
---
## LayoutOptions::get_ContinuousSectionPageNumberingRestart method


Ottiene o imposta la modalità di comportamento per il calcolo dei numeri di pagina quando una sezione continua riavvia la numerazione delle pagine.

```cpp
Aspose::Words::Layout::ContinuousSectionRestart Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart() const
```


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

* Enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
