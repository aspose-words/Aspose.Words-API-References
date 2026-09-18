---
title: "Aspose::Words::Document::get_ShowSpellingErrors-Methode"
linktitle: "get_ShowSpellingErrors"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_ShowSpellingErrors-Methode. Gibt an, ob Rechtschreibfehler in diesem Dokument in C++ angezeigt werden sollen."
type: docs
weight: 51000
url: /de/cpp/aspose.words/document/get_showspellingerrors/
---
## Document::get_ShowSpellingErrors method


Gibt an, ob Rechtschreibfehler in diesem Dokument angezeigt werden sollen.

```cpp
bool Aspose::Words::Document::get_ShowSpellingErrors()
```


## Beispiele



Zeigt, wie Fehler im Dokument ein- und ausgeblendet werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie zwei Sätze mit Fehlern ein, die erkannt werden würden
// von den Rechtschreib- und Grammatikprüfungen in Microsoft Word.
builder->Writeln(u"There is a speling error in this sentence.");
builder->Writeln(u"Their is a grammatical error in this sentence.");

// Wenn diese Optionen aktiviert sind, werden Rechtschreibfehler unterstrichen
// im Ausgabedokument durch eine gezackte rote Linie, und eine doppelte blaue Linie hebt grammatikalische Fehler hervor.
doc->set_ShowGrammaticalErrors(showErrors);
doc->set_ShowSpellingErrors(showErrors);

doc->Save(get_ArtifactsDir() + u"Document.SpellingAndGrammarErrors.docx");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
