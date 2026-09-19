---
title: "Metodo Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries"
linktitle: "get_DoNotDisplayPageBoundaries"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries. Disattiva la visualizzazione dello spazio tra la parte superiore del testo e il bordo superiore della pagina in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.settings/viewoptions/get_donotdisplaypageboundaries/
---
## ViewOptions::get_DoNotDisplayPageBoundaries method


Disattiva la visualizzazione dello spazio tra la parte superiore del testo e il bordo superiore della pagina.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries() const
```


## Esempi



Mostra come nascondere gli spazi verticali e le intestazioni/piè di pagina nelle opzioni di visualizzazione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci contenuto che si estende su 3 pagine.
builder->Writeln(u"Paragraph 1, Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 2, Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 3, Page 3.");

// Inserisci un'intestazione e un piè di pagina.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the footer.");

// Questo documento contiene una piccola quantità di contenuto che occupa lo spazio di alcune pagine intere.
// Imposta il flag "DoNotDisplayPageBoundaries" su "true" per fare in modo che le versioni più vecchie di Microsoft Word omettano le intestazioni,
// i piè di pagina e gran parte degli spazi verticali quando visualizziamo il nostro documento.
// Imposta il flag "DoNotDisplayPageBoundaries" su "false" per fare in modo che le versioni più vecchie di Microsoft Word
// visualizzino normalmente il nostro documento.
doc->get_ViewOptions()->set_DoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayPageBoundaries.doc");
```

## Vedi anche

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
