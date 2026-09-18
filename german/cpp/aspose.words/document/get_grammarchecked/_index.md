---
title: "Aspose::Words::Document::get_GrammarChecked Methode"
linktitle: "get_GrammarChecked"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_GrammarChecked Methode. Gibt true zurück, wenn das Dokument in C++ auf Grammatik geprüft wurde."
type: docs
weight: 29000
url: /de/cpp/aspose.words/document/get_grammarchecked/
---
## Document::get_GrammarChecked method


Gibt **true** zurück, wenn das Dokument auf Grammatik geprüft wurde.

```cpp
bool Aspose::Words::Document::get_GrammarChecked()
```


## Beispiele



Zeigt, wie die Rechtschreib- oder Grammatikprüfung eingestellt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Die Zeichenkette mit Rechtschreibfehlern.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"The speeling in this documentz is all broked."));

// Rechtschreib-/Grammatikprüfung startet, wenn wir die Eigenschaften auf false setzen.
// Wir können alle Fehler in Microsoft Word über Überprüfen -> Rechtschreibung & Grammatik sehen.
// Beachten Sie, dass Microsoft Word die Grammatik-/Rechtschreibprüfung für das DOC- und RTF-Dokumentformat nicht automatisch startet.
doc->set_SpellingChecked(checkSpellingGrammar);
doc->set_GrammarChecked(checkSpellingGrammar);

doc->Save(get_ArtifactsDir() + u"Document.SpellingOrGrammar.docx");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
