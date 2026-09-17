---
title: "Méthode Aspose::Words::Saving::FontSavingArgs::get_FontFileName"
linktitle: "get_FontFileName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::FontSavingArgs::get_FontFileName. Obtient ou définit le nom de fichier (sans le chemin) où la police sera enregistrée en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/fontsavingargs/get_fontfilename/
---
## FontSavingArgs::get_FontFileName method


Obtient ou définit le nom de fichier (sans le chemin) où la police sera enregistrée.

```cpp
System::String Aspose::Words::Saving::FontSavingArgs::get_FontFileName() const
```

## Remarques


Cette propriété vous permet de redéfinir la façon dont les noms de fichiers de police sont générés lors de l’exportation vers HTML.

Lorsque l’événement est déclenché, cette propriété contient le nom de fichier généré par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour enregistrer la police dans un fichier différent. Notez que les noms de fichiers doivent être uniques.

Aspose.Words génère automatiquement un nom de fichier unique pour chaque police incorporée lors de l’exportation au format HTML. La façon dont le nom de fichier de la police est généré dépend de si vous enregistrez le document dans un fichier ou dans un flux.

Lors de l’enregistrement d’un document dans un fichier, le nom de fichier de police généré ressemble à *%<document base file name>.<original file name><optional suffix>.<extension>*.

Lors de l’enregistrement d’un document dans un flux, le nom de fichier de police généré ressemble à *Aspose.Words.<document guid>.<original file name><optional suffix>.<extension>*.

[FontFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [FontsFolder](../../htmlsaveoptions/get_fontsfolder/) and [FontsFolderAlias](../../htmlsaveoptions/get_fontsfolderalias/) properties.

## Voir aussi

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
