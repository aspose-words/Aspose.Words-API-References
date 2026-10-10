---
title: "Classe Aspose::Words::Hyphenation"
linktitle: "Césure"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Hyphenation. Fournit des méthodes pour travailler avec les dictionnaires de césure. Ces dictionnaires indiquent où les mots d'une langue spécifique peuvent être césurés. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 33000
url: /fr/cpp/aspose.words/hyphenation/
---
## Hyphenation class


Fournit des méthodes pour travailler avec les dictionnaires de césure. Ces dictionnaires indiquent où les mots d'une langue spécifique peuvent être césurés. Pour en savoir plus, consultez l'article de documentation [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class Hyphenation
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [get_Callback](./get_callback/)() | Obtient l'interface de rappel utilisée pour demander les dictionnaires lors de la construction de la mise en page du document. Cela permet de charger les dictionnaires de manière différée, ce qui peut être utile lors du traitement de documents dans de nombreuses langues. |
| static [get_WarningCallback](./get_warningcallback/)() | Appelé lors du chargement des modèles de césure, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| [Hyphenation](./hyphenation/)() |  |
| static [IsDictionaryRegistered](./isdictionaryregistered/)(const System::String\&) | Renvoie **false** si, pour la langue spécifiée, aucun dictionnaire n'est enregistré ou si le dictionnaire enregistré est Null, **true** sinon. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) | Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir d'un flux. Lève une exception si le dictionnaire ne peut pas être lu ou a un format invalide. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::String\&) | Enregistre et charge un dictionnaire de césure pour la langue spécifiée à partir d'un fichier. Lève une exception si le dictionnaire ne peut pas être lu ou a un format invalide. Cette méthode peut également être utilisée pour enregistrer un dictionnaire Null afin d'empêcher [Callback](./get_callback/) d'être appelé de manière répétée pour la même langue. |
| static [RegisterDictionary](./registerdictionary/)(System::String, std::basic_istream\<CharType, Traits\>\&) |  |
| static [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::IHyphenationCallback\>\&) | Définit l'interface de rappel utilisée pour demander les dictionnaires lors de la construction de la mise en page du document. Cela permet de charger les dictionnaires de manière différée, ce qui peut être utile lors du traitement de documents dans de nombreuses langues. |
| static [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Appelé lors du chargement des modèles de césure, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| static [UnregisterDictionary](./unregisterdictionary/)(const System::String\&) | Désenregistre un dictionnaire de césure pour la langue spécifiée. Cela diffère de l'enregistrement d'un dictionnaire Null. Le désenregistrement d'un dictionnaire active le rappel pour la langue spécifiée. |
## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
