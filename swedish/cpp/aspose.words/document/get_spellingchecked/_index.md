---
title: "Aspose::Words::Document::get_SpellingChecked metod"
linktitle: "get_SpellingChecked"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_SpellingChecked metod. Returnerar true om dokumentet har kontrollerats för stavning i C++."
type: docs
weight: 52000
url: /sv/cpp/aspose.words/document/get_spellingchecked/
---
## Document::get_SpellingChecked method


Returnerar **true** om dokumentet har kontrollerats för stavning.

```cpp
bool Aspose::Words::Document::get_SpellingChecked()
```


## Exempel



Visar hur man ställer in stavnings- eller grammatikkontroll.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Strängen med stavfel.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"The speeling in this documentz is all broked."));

// Stavnings-/grammatikgranskning startar om vi sätter egenskaperna till false.
// Vi kan se alla fel i Microsoft Word via Granska -> Stavning & Grammatik.
// Observera att Microsoft Word inte startar grammatik-/stavningskontroll automatiskt för DOC- och RTF-dokumentformat.
doc->set_SpellingChecked(checkSpellingGrammar);
doc->set_GrammarChecked(checkSpellingGrammar);

doc->Save(get_ArtifactsDir() + u"Document.SpellingOrGrammar.docx");
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
