---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly method"
linktitle: "get_FindWholeWordsOnly"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly method. True indique que oldValue doit être un mot autonome en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_findwholewordsonly/
---
## FindReplaceOptions::get_FindWholeWordsOnly method


True indique que oldValue doit être un mot autonome.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly() const
```


## Exemples



Montre comment activer/désactiver les opérations de recherche et remplacement limitées aux mots isolés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez le drapeau "FindWholeWordsOnly" sur "true" pour remplacer le texte trouvé s'il ne fait pas partie d'un autre mot.
// Définissez le drapeau "FindWholeWordsOnly" sur "false" pour remplacer tout le texte, quel que soit son contexte.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
