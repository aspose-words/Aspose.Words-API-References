---
title: "Aspose::Words::Document::get_SpellingChecked méthode"
linktitle: "get_SpellingChecked"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_SpellingChecked méthode. Retourne true si le document a été vérifié pour l'orthographe en C++."
type: docs
weight: 52000
url: /fr/cpp/aspose.words/document/get_spellingchecked/
---
## Document::get_SpellingChecked method


Renvoie **true** si le document a été vérifié pour l'orthographe.

```cpp
bool Aspose::Words::Document::get_SpellingChecked()
```


## Exemples



Montre comment activer la vérification de l'orthographe ou de la grammaire.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// La chaîne contenant des fautes d'orthographe.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"The speeling in this documentz is all broked."));

// La vérification orthographe/grammaire démarre si nous définissons les propriétés sur false.
// Nous pouvons voir toutes les erreurs dans Microsoft Word via Révision -> Orthographe et grammaire.
// Notez que Microsoft Word ne lance pas automatiquement la vérification grammaticale/orthographique pour les formats de document DOC et RTF.
doc->set_SpellingChecked(checkSpellingGrammar);
doc->set_GrammarChecked(checkSpellingGrammar);

doc->Save(get_ArtifactsDir() + u"Document.SpellingOrGrammar.docx");
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
