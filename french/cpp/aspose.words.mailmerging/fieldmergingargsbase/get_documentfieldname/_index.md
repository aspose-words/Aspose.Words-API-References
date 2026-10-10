---
title: "Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName méthode"
linktitle: "get_DocumentFieldName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName méthode. Obtient le nom du champ de fusion tel qu'il est spécifié dans le document en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.mailmerging/fieldmergingargsbase/get_documentfieldname/
---
## FieldMergingArgsBase::get_DocumentFieldName method


Obtient le nom du champ de fusion tel qu’il est spécifié dans le document.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName() const
```

## Remarques


Si vous avez une correspondance d'un nom de champ de document vers un nom de champ de source de données différent, alors il s'agit du nom de champ original tel qu'il est spécifié dans le document.

Si vous avez spécifié un préfixe de nom de champ, par exemple "Image:MyFieldName" dans le document, alors [DocumentFieldName](./) renvoie le nom du champ sans le préfixe, c'est-à-dire "MyFieldName".
## Voir aussi

* Class [FieldMergingArgsBase](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
