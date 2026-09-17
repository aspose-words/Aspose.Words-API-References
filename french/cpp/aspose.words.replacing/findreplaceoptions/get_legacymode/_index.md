---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode méthode"
linktitle: "get_LegacyMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode méthode. Obtient ou définit une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_legacymode/
---
## FindReplaceOptions::get_LegacyMode method


Obtient ou définit une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode() const
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

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
