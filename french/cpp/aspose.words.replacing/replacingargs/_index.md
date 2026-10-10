---
title: "Classe Aspose::Words::Replacing::ReplacingArgs"
linktitle: "ReplacingArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Replacing::ReplacingArgs. Fournit des données pour une opération de remplacement personnalisée. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class


Fournit des données pour une opération de remplacement personnalisée. Pour en savoir plus, consultez l'article de documentation [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/).

```cpp
class ReplacingArgs : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_GroupIndex](./get_groupindex/)() const | Identifie, par indice, un groupe capturé dans le [Match](./get_match/) qui doit être remplacé par la chaîne [Replacement](./get_replacement/). |
| [get_GroupName](./get_groupname/)() const | Identifie, par nom, un groupe capturé dans le [Match](./get_match/) qui doit être remplacé par la chaîne [Replacement](./get_replacement/). |
| [get_Match](./get_match/)() const | Le **Match** résultant d'une correspondance unique d'expression régulière pendant un **Replace**. |
| [get_MatchEndNode](./get_matchendnode/)() const | Obtient le nœud qui contient la fin de la correspondance. |
| [get_MatchNode](./get_matchnode/)() const | Obtient le nœud qui contient le début de la correspondance. |
| [get_MatchOffset](./get_matchoffset/)() const | Obtient la position de départ à base zéro de la correspondance à partir du début du nœud qui contient le début de la correspondance. |
| [get_Replacement](./get_replacement/)() const | Obtient la chaîne de remplacement. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GroupIndex](./set_groupindex/)(int32_t) | Mutateur pour [Aspose::Words::Replacing::ReplacingArgs::get_GroupIndex](./get_groupindex/). |
| [set_GroupName](./set_groupname/)(const System::String\&) | Mutateur pour [Aspose::Words::Replacing::ReplacingArgs::get_GroupName](./get_groupname/). |
| [set_Replacement](./set_replacement/)(const System::String\&) | Définit la chaîne de remplacement. |
| static [Type](./type/)() |  |

## Voir aussi

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
