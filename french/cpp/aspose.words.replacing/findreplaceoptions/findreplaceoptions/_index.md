---
title: "Constructeur Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Constructeur Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions. Initialise une nouvelle instance de la classe FindReplaceOptions avec les paramètres par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions::FindReplaceOptions() constructor


Initialise une nouvelle instance de la classe [FindReplaceOptions](../) avec les paramètres par défaut.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions()
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
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection) constructor


Initialise une nouvelle instance de la classe [FindReplaceOptions](../) avec la direction spécifiée.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| direction | Aspose::Words::Replacing::FindReplaceDirection | La direction de l'opération de recherche et remplacement. |

## Voir aussi

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Initialise une nouvelle instance de la classe [FindReplaceOptions](../) avec la direction spécifiée et le rappel de remplacement.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction, const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| direction | Aspose::Words::Replacing::FindReplaceDirection | La direction de l'opération de recherche et remplacement. |
| replacingCallback | const System::SharedPtr\\<Aspose::Words::Replacing::IReplacingCallback\\>\\& | Le rappel à utiliser pour remplacer le texte trouvé. |

## Voir aussi

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Initialise une nouvelle instance de la classe [FindReplaceOptions](../) avec le rappel de remplacement spécifié.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| replacingCallback | const System::SharedPtr\\<Aspose::Words::Replacing::IReplacingCallback\\>\\& | Le rappel à utiliser pour remplacer le texte trouvé. |

## Voir aussi

* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
