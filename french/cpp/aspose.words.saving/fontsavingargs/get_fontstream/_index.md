---
title: "Méthode Aspose::Words::Saving::FontSavingArgs::get_FontStream"
linktitle: "get_FontStream"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::FontSavingArgs::get_FontStream. Permet de spécifier le flux où la police sera enregistrée en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/fontsavingargs/get_fontstream/
---
## FontSavingArgs::get_FontStream method


Permet de spécifier le flux où la police sera enregistrée.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::FontSavingArgs::get_FontStream() const
```

## Remarques


Cette propriété vous permet d’enregistrer les polices dans des flux au lieu de fichiers lors de l’exportation HTML.

La valeur par défaut est **null**. Lorsque cette propriété est **null**, la police sera enregistrée dans un fichier spécifié dans la propriété [FontFileName](../get_fontfilename/).

## Voir aussi

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
