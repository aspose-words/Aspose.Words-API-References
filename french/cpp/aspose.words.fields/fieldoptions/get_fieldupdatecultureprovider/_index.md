---
title: "Méthode Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider"
linktitle: "get_FieldUpdateCultureProvider"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider. Obtient ou définit un fournisseur qui renvoie un objet de culture spécifique à chaque champ particulier en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.fields/fieldoptions/get_fieldupdatecultureprovider/
---
## FieldOptions::get_FieldUpdateCultureProvider method


Obtient ou définit un fournisseur qui renvoie un objet de culture spécifique à chaque champ particulier.

```cpp
const System::SharedPtr<Aspose::Words::Fields::IFieldUpdateCultureProvider> & Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider() const
```

## Remarques


Le fournisseur est demandé lorsque la valeur de [FieldUpdateCultureSource](../get_fieldupdateculturesource/) est [FieldCode](../../fieldupdateculturesource/).

Si le fournisseur est présent, alors l'objet de culture qu'il renvoie est utilisé pour la mise à jour du champ. Sinon, une culture système est utilisée.
## Voir aussi

* Interface [IFieldUpdateCultureProvider](../../ifieldupdatecultureprovider/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
