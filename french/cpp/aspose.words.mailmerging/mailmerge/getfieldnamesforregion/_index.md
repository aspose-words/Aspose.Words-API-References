---
title: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion méthode"
linktitle: "GetFieldNamesForRegion"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion méthode. Renvoie une collection de noms de champs de fusion de courrier disponibles dans la région en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## MailMerge::GetFieldNamesForRegion(const System::String\&) method


Renvoie une collection de noms de champs de fusion de courrier disponibles dans la région.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| regionName | const System::String\& | Nom de la région (insensible à la casse). |
## Remarques


Renvoie les noms complets des champs de fusion, y compris le préfixe optionnel. N'élimine pas les noms de champs en double.

Si le document contient plusieurs régions portant le même nom, la toute première région est traitée.

Un nouveau tableau de chaînes est créé à chaque appel.

## Voir aussi

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::GetFieldNamesForRegion(const System::String\&, int32_t) method


Renvoie une collection de noms de champs de fusion de courrier disponibles dans la région.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName, int32_t regionIndex)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| regionName | const System::String\& | Nom de la région (insensible à la casse). |
| regionIndex | int32_t | Indice de la région (à base zéro). |
## Remarques


Renvoie les noms complets des champs de fusion, y compris le préfixe optionnel. N'élimine pas les noms de champs en double.

Si le document contient plusieurs régions portant le même nom, la Nᵉ région (à base zéro) est traitée.

Un nouveau tableau de chaînes est créé à chaque appel.

## Voir aussi

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
