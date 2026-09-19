---
title: "Aspose::Words::Document::get_GrammarChecked metodo"
linktitle: "get_GrammarChecked"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_GrammarChecked metodo. Restituisce true se il documento è stato controllato per la grammatica in C++."
type: docs
weight: 29000
url: /it/cpp/aspose.words/document/get_grammarchecked/
---
## Document::get_GrammarChecked method


Restituisce **true** se il documento è stato controllato per la grammatica.

```cpp
bool Aspose::Words::Document::get_GrammarChecked()
```


## Esempi



Mostra come impostare la verifica ortografica o grammaticale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// La stringa con errori ortografici.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"The speeling in this documentz is all broked."));

// Il controllo ortografia/grammatica inizia se impostiamo le proprietà su false.
// Possiamo vedere tutti gli errori in Microsoft Word tramite Revisione -> Ortografia e grammatica.
// Nota che Microsoft Word non avvia automaticamente il controllo grammaticale/ortografico per i formati di documento DOC e RTF.
doc->set_SpellingChecked(checkSpellingGrammar);
doc->set_GrammarChecked(checkSpellingGrammar);

doc->Save(get_ArtifactsDir() + u"Document.SpellingOrGrammar.docx");
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
