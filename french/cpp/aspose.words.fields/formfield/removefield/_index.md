---
title: "Méthode Aspose::Words::Fields::FormField::RemoveField"
linktitle: "RemoveField"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FormField::RemoveField. Supprime le champ de formulaire complet, pas seulement le caractère spécial du champ de formulaire en C++."
type: docs
weight: 27000
url: /fr/cpp/aspose.words.fields/formfield/removefield/
---
## FormField::RemoveField method


Supprime le champ de formulaire complet, pas seulement le caractère spécial du champ de formulaire.

```cpp
void Aspose::Words::Fields::FormField::RemoveField()
```


## Exemples



Montre comment supprimer un champ de formulaire.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(3);
formField->RemoveField();
```

## Voir aussi

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
