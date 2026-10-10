---
title: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields méthode"
linktitle: "get_PreserveFormFields"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields méthode. Spécifie si les champs de formulaire Microsoft Word doivent être conservés en tant que champs de formulaire dans le PDF ou convertis en texte. La valeur par défaut est false en C++."
type: docs
weight: 28000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_preserveformfields/
---
## PdfSaveOptions::get_PreserveFormFields method


Spécifie s'il faut conserver les champs de formulaire Microsoft Word en tant que champs de formulaire dans le PDF ou les convertir en texte. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields() const
```

## Remarques


Les champs de formulaire Microsoft Word comprennent des contrôles de saisie de texte, de liste déroulante et de case à cocher.

Lorsque la valeur est **false**, ces champs seront exportés en texte vers le PDF. Lorsque la valeur est **true**, ces champs seront exportés en tant que champs de formulaire PDF.

Lors de l'exportation des champs de formulaire vers le PDF en tant que champs de formulaire, une perte de mise en forme peut survenir parce que les champs de formulaire PDF ne prennent pas en charge toutes les fonctionnalités des champs de formulaire Microsoft Word.

De plus, la taille du résultat dépend de la taille du contenu car les formulaires modifiables dans Microsoft Word sont des objets en ligne.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
