---
title: "Méthode Aspose::Words::Fields::FormFieldCollection::idx_get"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FormFieldCollection::idx_get. Retourne un champ de formulaire par nom de signet en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.fields/formfieldcollection/idx_get/
---
## FormFieldCollection::idx_get(const System::String\&) method


Renvoie un champ de formulaire par le nom du signet.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::Fields::FormFieldCollection::idx_get(const System::String &bookmarkName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | Nom de signet insensible à la casse. |

## Voir aussi

* Class [FormField](../../formfield/)
* Class [FormFieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FormFieldCollection::idx_get(int32_t) method


Renvoie un champ de formulaire à l'index spécifié.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::Fields::FormFieldCollection::idx_get(int32_t index)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | Un index dans la collection. |
## Remarques


L'index commence à zéro.

Les index négatifs sont autorisés et indiquent un accès depuis la fin de la collection. Par exemple, -1 signifie le dernier élément, -2 le deuxième avant le dernier, etc.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

## Voir aussi

* Class [FormField](../../formfield/)
* Class [FormFieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
