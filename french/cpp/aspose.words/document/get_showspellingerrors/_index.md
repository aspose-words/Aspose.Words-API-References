---
title: "Aspose::Words::Document::get_ShowSpellingErrors méthode"
linktitle: "get_ShowSpellingErrors"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_ShowSpellingErrors méthode. Spécifie s'il faut afficher les fautes d'orthographe dans ce document en C++."
type: docs
weight: 51000
url: /fr/cpp/aspose.words/document/get_showspellingerrors/
---
## Document::get_ShowSpellingErrors method


Spécifie s'il faut afficher les fautes d'orthographe dans ce document.

```cpp
bool Aspose::Words::Document::get_ShowSpellingErrors()
```


## Exemples



Montre comment afficher/masquer les erreurs dans le document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez deux phrases contenant des erreurs qui seraient détectées
// par les correcteurs d'orthographe et de grammaire de Microsoft Word.
builder->Writeln(u"There is a speling error in this sentence.");
builder->Writeln(u"Their is a grammatical error in this sentence.");

// Si ces options sont activées, les fautes d'orthographe seront soulignées
// dans le document de sortie par une ligne rouge en pointillés, et une double ligne bleue mettra en évidence les erreurs grammaticales.
doc->set_ShowGrammaticalErrors(showErrors);
doc->set_ShowSpellingErrors(showErrors);

doc->Save(get_ArtifactsDir() + u"Document.SpellingAndGrammarErrors.docx");
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
