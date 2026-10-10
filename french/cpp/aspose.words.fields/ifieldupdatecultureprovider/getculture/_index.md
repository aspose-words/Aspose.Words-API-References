---
title: "Méthode Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture"
linktitle: "GetCulture"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture. Retourne un objet CultureInfo à utiliser pendant la mise à jour du champ en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider::GetCulture method


Renvoie un objet **CultureInfo** à utiliser lors de la mise à jour du champ.

```cpp
virtual System::SharedPtr<System::Globalization::CultureInfo> Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture(System::String culture, System::SharedPtr<Aspose::Words::Fields::Field> field)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| culture | System::String | Le nom de la culture demandée pour le champ en cours de mise à jour. |
| champ | System::SharedPtr\<Aspose::Words::Fields::Field\> | Le champ en cours de mise à jour. |

### ReturnValue

L'objet culture qui doit être utilisé pour la mise à jour du champ.

## Voir aussi

* Class [Field](../../field/)
* Interface [IFieldUpdateCultureProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
