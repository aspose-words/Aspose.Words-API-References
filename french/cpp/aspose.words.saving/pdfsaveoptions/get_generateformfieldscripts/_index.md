---
title: "méthode Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts"
linktitle: "get_GenerateFormFieldScripts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts. Spécifie s’il faut générer des scripts qui reproduisent le comportement spécifique des champs de formulaire Microsoft Word dans le PDF. La valeur par défaut est false en C++."
type: docs
weight: 18500
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_generateformfieldscripts/
---
## PdfSaveOptions::get_GenerateFormFieldScripts method


Spécifie s'il faut générer des scripts qui émulent le comportement spécifique des champs de formulaire Microsoft Word dans le PDF. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts() const
```

## Remarques


Lorsque cette option est activée, l’exportateur génère des actions JavaScript PDF pour reproduire le comportement des champs de formulaire Microsoft Word, tels que les champs de date et d’heure avec des règles de formatage et de validation.

Lorsqu’elle est définie sur **true**, le comportement pris en charge sera exporté sous forme d’actions JavaScript PDF. Lorsqu’elle est définie sur **false**, aucun script de champ de formulaire ne sera généré.

L’exécution des scripts dépend du visualiseur PDF. Certains visualiseurs PDF peuvent ignorer les scripts, restreindre leur exécution ou obliger l’utilisateur à activer JavaScript.

Les actions JavaScript sont interdites par la conformité PDF/A-1, PDF/A-2 et PDF/A-3. La valeur **false** sera utilisée automatiquement dans ce cas.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
