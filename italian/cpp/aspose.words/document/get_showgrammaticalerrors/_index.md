---
title: "Metodo Aspose::Words::Document::get_ShowGrammaticalErrors"
linktitle: "get_ShowGrammaticalErrors"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_ShowGrammaticalErrors. Specifica se visualizzare gli errori grammaticali in questo documento in C++."
type: docs
weight: 50000
url: /it/cpp/aspose.words/document/get_showgrammaticalerrors/
---
## Document::get_ShowGrammaticalErrors method


Specifica se visualizzare gli errori grammaticali in questo documento.

```cpp
bool Aspose::Words::Document::get_ShowGrammaticalErrors()
```


## Esempi



Mostra come mostrare/nascondere gli errori nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci due frasi con errori che verrebbero rilevati
// dal correttore ortografico e grammaticale di Microsoft Word.
builder->Writeln(u"There is a speling error in this sentence.");
builder->Writeln(u"Their is a grammatical error in this sentence.");

// Se queste opzioni sono abilitate, gli errori ortografici saranno sottolineati
// nel documento di output da una linea rossa a zigzag, e una doppia linea blu evidenzierà gli errori grammaticali.
doc->set_ShowGrammaticalErrors(showErrors);
doc->set_ShowSpellingErrors(showErrors);

doc->Save(get_ArtifactsDir() + u"Document.SpellingAndGrammarErrors.docx");
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
