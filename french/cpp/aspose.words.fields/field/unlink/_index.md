---
title: "Aspose::Words::Fields::Field::Unlink méthode"
linktitle: "Dissocier"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::Field::Unlink méthode. Effectue la dissociation du champ en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words.fields/field/unlink/
---
## Field::Unlink method


Effectue le détachement du champ.

```cpp
bool Aspose::Words::Fields::Field::Unlink()
```


### ReturnValue

**true** if the field has been unlinked, otherwise **false**.
## Remarques


Remplace le champ par son résultat le plus récent.

Certains champs, tels que les champs XE (Entrée d'index) et SEQ (Séquence), ne peuvent pas être dissociés.

## Exemples



Montre comment dissocier un champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");
doc->get_Range()->get_Fields()->idx_get(1)->Unlink();
```

## Voir aussi

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
