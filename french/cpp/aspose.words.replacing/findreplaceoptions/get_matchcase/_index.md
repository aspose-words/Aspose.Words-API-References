---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase méthode"
linktitle: "get_MatchCase"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase méthode. True indique une comparaison sensible à la casse, false indique une comparaison insensible à la casse en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_matchcase/
---
## FindReplaceOptions::get_MatchCase method


True indique une comparaison sensible à la casse, false indique une comparaison insensible à la casse.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase() const
```


## Exemples



Montre comment activer/désactiver la sensibilité à la casse lors d'une opération de recherche et remplacement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez le drapeau "MatchCase" sur "true" pour appliquer la sensibilité à la casse lors de la recherche des chaînes à remplacer.
// Définissez le drapeau "MatchCase" sur "false" pour ignorer la casse des caractères lors de la recherche du texte à remplacer.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
