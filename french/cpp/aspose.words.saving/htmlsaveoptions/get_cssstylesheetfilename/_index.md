---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName méthode"
linktitle: "get_CssStyleSheetFileName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName méthode. Spécifie le chemin et le nom du fichier de feuille de style en cascade (CSS) écrit lorsqu'un document est exporté vers HTML. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheetfilename/
---
## HtmlSaveOptions::get_CssStyleSheetFileName method


Spécifie le chemin et le nom du fichier de feuille de style en cascade [Style](../../../aspose.words/style/) (CSS) écrit lorsqu'un document est exporté vers HTML. La valeur par défaut est une chaîne vide.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName() const
```

## Remarques


Cette propriété n'a d'effet que lors de l'enregistrement d'un document au format HTML et qu'une feuille de style CSS externe est demandée en utilisant [CssStyleSheetType](../get_cssstylesheettype/).

Si cette propriété est vide, le fichier CSS sera enregistré dans le même dossier et avec le même nom que le document HTML mais avec l'extension ".css".

Si seul le chemin mais aucun nom de fichier n'est spécifié dans cette propriété, le fichier CSS sera enregistré dans le dossier indiqué et aura le même nom que le document HTML mais avec l'extension ".css".

Si le dossier indiqué par cette propriété n'existe pas, il sera créé automatiquement avant l'enregistrement du fichier CSS.

Une autre façon de spécifier un dossier où le fichier CSS externe est enregistré consiste à utiliser [ResourceFolder](../get_resourcefolder/).

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
