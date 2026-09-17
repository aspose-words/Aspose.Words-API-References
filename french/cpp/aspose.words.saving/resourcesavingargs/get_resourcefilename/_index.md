---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName méthode"
linktitle: "get_ResourceFileName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName méthode. Obtient ou définit le nom de fichier (sans le chemin) où la ressource sera enregistrée en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/resourcesavingargs/get_resourcefilename/
---
## ResourceSavingArgs::get_ResourceFileName method


Obtient ou définit le nom de fichier (sans le chemin) où la ressource sera enregistrée.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName() const
```

## Remarques


Cette propriété vous permet de redéfinir la façon dont les noms de fichiers de ressources sont générés lors de l'exportation vers HTML à page fixe, SVG ou Markdown.

Lorsque l'événement est déclenché, cette propriété contient le nom de fichier généré par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour enregistrer la ressource dans un fichier différent. Notez que les noms de fichiers doivent être uniques.

Aspose.Words génère automatiquement un nom de fichier unique pour chaque ressource lors de l'exportation au format HTML à page fixe, SVG ou Markdown. La façon dont le nom de fichier de la ressource est généré dépend de si vous enregistrez le document dans un fichier ou dans un flux.

Lors de l'enregistrement d'un document dans un fichier, le nom de fichier de ressource généré ressemble à *%<document base file name>.<image number>.<extension>*.

Lors de l'enregistrement d'un document dans un flux, le nom de fichier de ressource généré ressemble à *Aspose.Words.<document guid>.<image number>.<extension>*.

[ResourceFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [ResourcesFolder](../../htmlfixedsaveoptions/get_resourcesfolder/) or [ResourcesFolder](../../svgsaveoptions/get_resourcesfolder/) and [ResourcesFolderAlias](../../htmlfixedsaveoptions/get_resourcesfolderalias/) or [ResourcesFolderAlias](../../svgsaveoptions/get_resourcesfolderalias/) or [ImagesFolder](../../markdownsaveoptions/get_imagesfolder/) or [ImagesFolderAlias](../../markdownsaveoptions/get_imagesfolderalias/) properties.

## Voir aussi

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
