---
title: "Méthode Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream"
linktitle: "get_ResourceStream"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream. Permet de spécifier le flux où la ressource sera enregistrée en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/resourcesavingargs/get_resourcestream/
---
## ResourceSavingArgs::get_ResourceStream method


Permet de spécifier le flux où la ressource sera enregistrée.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream() const
```

## Remarques


Cette propriété vous permet d’enregistrer des ressources dans des flux au lieu de fichiers.

La valeur par défaut est **null**. Lorsque cette propriété est **null**, la ressource sera enregistrée dans un fichier spécifié dans la propriété [ResourceFileName](../get_resourcefilename/).

En utilisant [IResourceSavingCallback](../../iresourcesavingcallback/), vous ne pouvez pas substituer une ressource par une autre. Il est destiné uniquement au contrôle de l’emplacement où enregistrer les ressources.

## Voir aussi

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
