---
title: "Méthode idx_get de Aspose::Words::RevisionGroupCollection"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode idx_get de Aspose::Words::RevisionGroupCollection. Retourne un groupe de révisions à l'index spécifié en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/revisiongroupcollection/idx_get/
---
## RevisionGroupCollection::idx_get method


Renvoie un groupe de révisions à l'index spécifié.

```cpp
System::SharedPtr<Aspose::Words::RevisionGroup> Aspose::Words::RevisionGroupCollection::idx_get(int32_t index)
```


## Exemples



Montre comment obtenir un groupe de révisions dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## Voir aussi

* Class [RevisionGroup](../../revisiongroup/)
* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
