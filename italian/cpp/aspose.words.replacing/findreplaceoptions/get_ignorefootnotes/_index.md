---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes metodo"
linktitle: "get_IgnoreFootnotes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes. Ottiene o imposta un valore booleano che indica se ignorare le note a piè di pagina. Il valore predefinito è false in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefootnotes/
---
## FindReplaceOptions::get_IgnoreFootnotes method


Ottiene o imposta un valore booleano che indica se ignorare le note a piè di pagina. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes() const
```


## Esempi



Mostra come ignorare le note a piè di pagina durante un'operazione di ricerca e sostituzione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder->InsertParagraph();

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Imposta il flag "IgnoreFootnotes" su "true" per ottenere la ricerca e sostituzione
// operazione per ignorare il testo all'interno delle note a piè di pagina.
// Imposta il flag "IgnoreFootnotes" su "false" per ottenere la ricerca e sostituzione
// operazione per cercare anche il testo all'interno delle note a piè di pagina.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFootnotes(isIgnoreFootnotes);
doc->get_Range()->Replace(u"Lorem ipsum", u"Replaced Lorem ipsum", options);
```

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
