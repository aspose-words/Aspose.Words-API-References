---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName méthode"
linktitle: "get_UseSdtTagAsFormFieldName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName méthode. Spécifie s'il faut utiliser la propriété Tag ou Id du contrôle SDT comme nom de champ de formulaire dans le PDF en C++."
type: docs
weight: 32500
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_usesdttagasformfieldname/
---
## PdfSaveOptions::get_UseSdtTagAsFormFieldName method


Spécifie s'il faut utiliser la balise Tag ou la propriété Id du contrôle SDT comme nom du champ de formulaire dans le PDF.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName() const
```

## Remarques


La valeur par défaut est **false**.

Lorsqu'elle est définie sur **false**, la propriété Id du contrôle SDT est utilisée comme nom de champ de formulaire dans le PDF.

Lorsqu'elle est définie sur **true**, la propriété Tag du contrôle SDT est utilisée comme nom de champ de formulaire dans le PDF.

Si elle est définie sur **true** et que Tag est vide, la propriété Id sera utilisée comme nom de champ de formulaire.

Si elle est définie sur **true** et que les valeurs de Tag ne sont pas uniques, les valeurs de Tag en double seront modifiées pour créer des noms de champs de formulaire PDF uniques.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
