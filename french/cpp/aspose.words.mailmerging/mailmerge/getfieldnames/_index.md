---
title: "Aspose::Words::MailMerging::MailMerge::GetFieldNames méthode"
linktitle: "GetFieldNames"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::MailMerging::MailMerge::GetFieldNames méthode. Renvoie une collection de noms de champs de fusion de courrier disponibles dans le document en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge::GetFieldNames method


Renvoie une collection de noms de champs de fusion de courrier disponibles dans le document.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNames()
```

## Remarques


Renvoie les noms complets des champs de fusion, y compris le préfixe optionnel. N'élimine pas les noms de champs en double.

Un nouveau tableau de chaînes est créé à chaque appel.

Inclut les noms de champs "mustache" si [UseNonMergeFields](../get_usenonmergefields/) est **true**.
## Voir aussi

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
