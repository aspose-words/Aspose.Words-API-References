---
title: "Méthode Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded"
linktitle: "get_IsSubsettingNeeded"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded. Permet de spécifier si la police actuelle sera sous‑ensemble avant d’être exportée en tant que ressource de police en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.saving/fontsavingargs/get_issubsettingneeded/
---
## FontSavingArgs::get_IsSubsettingNeeded method


Permet de spécifier si la police actuelle sera sous‑ensemble avant d'être exportée en tant que ressource de police.

```cpp
bool Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded() const
```

## Remarques


[Fonts](../../../aspose.words.fonts/) can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

Par défaut, Aspose.Words décide d’effectuer ou non le sous‑ensemble en comparant la taille du fichier de police original avec celle spécifiée dans [FontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/get_fontresourcessubsettingsizethreshold/). Vous pouvez remplacer ce comportement pour des polices individuelles en définissant la propriété [IsSubsettingNeeded](./).
## Voir aussi

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
