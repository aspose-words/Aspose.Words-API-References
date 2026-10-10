---
title: "Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder méthode"
linktitle: "get_ResourcesFolder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder méthode. Spécifie le dossier physique où les ressources (images et polices) sont enregistrées lors de l’exportation d’un document au format Xaml à page fixe. La valeur par défaut est null en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/xamlfixedsaveoptions/get_resourcesfolder/
---
## XamlFixedSaveOptions::get_ResourcesFolder method


Spécifie le dossier physique où les ressources (images et polices) sont enregistrées lors de l’exportation d’un document au format Xaml à page fixe. La valeur par défaut est **null**.

```cpp
System::String Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder() const
```

## Remarques


Lorsque vous enregistrez un [Document](../../../aspose.words/document/) au format Xaml à page fixe, Aspose.Words doit enregistrer toutes les images incorporées dans le document en fichiers autonomes. [ResourcesFolder](./) vous permet de spécifier où les images seront enregistrées et [ResourcesFolderAlias](../get_resourcesfolderalias/) permet de spécifier comment les URI des images seront construites.

Si vous enregistrez un document dans un fichier et fournissez un nom de fichier, Aspose.Words, par défaut, enregistre les images dans le même dossier où le fichier du document est enregistré. Utilisez [ResourcesFolder](./) pour remplacer ce comportement.

Si vous enregistrez un document dans un flux, Aspose.Words n’a pas de dossier où enregistrer les images, mais doit tout de même les enregistrer quelque part. Dans ce cas, vous devez spécifier un dossier accessible en utilisant la propriété [ResourcesFolder](./).

## Voir aussi

* Class [XamlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
