---
title: "Méthode Aspose::Words::MailMerging::FieldMergingArgsBase::get_FieldName"
linktitle: "get_FieldName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::MailMerging::FieldMergingArgsBase::get_FieldName. Obtient le nom du champ de fusion dans la source de données en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.mailmerging/fieldmergingargsbase/get_fieldname/
---
## FieldMergingArgsBase::get_FieldName method


Obtient le nom du champ de fusion dans la source de données.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgsBase::get_FieldName() const
```

## Remarques


Si vous avez une correspondance entre le nom d’un champ du document et un nom de champ différent dans la source de données, alors il s’agit du nom de champ mappé.

Si vous avez spécifié un préfixe de nom de champ, par exemple "Image:MyFieldName" dans le document, alors [FieldName](./) renvoie le nom du champ sans le préfixe, c’est‑à‑dire "MyFieldName".
## Voir aussi

* Class [FieldMergingArgsBase](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
