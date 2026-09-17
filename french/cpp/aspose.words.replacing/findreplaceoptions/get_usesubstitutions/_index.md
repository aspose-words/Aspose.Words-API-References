---
title: "Méthode Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions"
linktitle: "get_UseSubstitutions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions. Obtient ou définit une valeur booléenne indiquant s'il faut reconnaître et utiliser les substitutions dans les modèles de remplacement. La valeur par défaut est false en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_usesubstitutions/
---
## FindReplaceOptions::get_UseSubstitutions method


Obtient ou définit une valeur booléenne indiquant s'il faut reconnaître et utiliser les substitutions dans les modèles de remplacement. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions() const
```


## Exemples



Montre comment reconnaître et utiliser les substitutions dans les modèles de remplacement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// L'utilisation du mode hérité ne prend pas en charge de nombreuses fonctionnalités avancées, nous devons donc le définir sur 'false'.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```


Montre comment remplacer le texte avec des substitutions.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"John sold a car to Paul.");
builder->Writeln(u"Jane sold a house to Joe.");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez la propriété "UseSubstitutions" sur "true" pour obtenir
// l'opération de recherche et remplacement afin de reconnaître les éléments de substitution.
// Définissez la propriété "UseSubstitutions" sur "false" pour ignorer les éléments de substitution.
options->set_UseSubstitutions(useSubstitutions);

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc->get_Range()->Replace(regex, u"$3 bought a $2 from $1", options);

ASSERT_EQ(useSubstitutions ? System::String(u"Paul bought a car from John.\rJoe bought a house from Jane.") : System::String(u"$3 bought a $2 from $1.\r$3 bought a $2 from $1."), doc->GetText().Trim());
```

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
