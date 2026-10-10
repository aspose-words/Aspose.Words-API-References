---
title: "Aspose::Words::Saving::CssSavingArgs::get_CssStream méthode"
linktitle: "get_CssStream"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::CssSavingArgs::get_CssStream method. Permet de spécifier le flux où les informations CSS seront enregistrées en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.saving/csssavingargs/get_cssstream/
---
## CssSavingArgs::get_CssStream method


Permet de spécifier le flux où les informations CSS seront enregistrées.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::CssSavingArgs::get_CssStream() const
```

## Remarques


Cette propriété vous permet d'enregistrer les informations CSS dans un flux.

La valeur par défaut est **null**. Cette propriété ne supprime pas l'enregistrement des informations CSS dans un fichier ou l'intégration dans le document HTML. Pour supprimer l'exportation du CSS, utilisez la propriété [IsExportNeeded](../get_isexportneeded/).

En utilisant [ICssSavingCallback](../../icsssavingcallback/), vous ne pouvez pas substituer le CSS par un autre. Il est destiné uniquement à l'enregistrement du CSS dans un flux.

## Voir aussi

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
