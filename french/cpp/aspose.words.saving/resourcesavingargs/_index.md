---
title: "Aspose::Words::Saving::ResourceSavingArgs classe"
linktitle: "ResourceSavingArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ResourceSavingArgs classe. Fournit des données pour l'événement ResourceSaving(). Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 27000
url: /fr/cpp/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class


Fournit des données pour l'événement [ResourceSaving()](../iresourcesavingcallback/resourcesaving/). Pour en savoir plus, consultez l'article de documentation [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ResourceSavingArgs : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Document](./get_document/)() const | Obtient l'objet document qui est actuellement en cours d'enregistrement. |
| [get_KeepResourceStreamOpen](./get_keepresourcestreamopen/)() const | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une ressource. |
| [get_ResourceFileName](./get_resourcefilename/)() const | Obtient ou définit le nom de fichier (sans le chemin) où la ressource sera enregistrée. |
| [get_ResourceFileUri](./get_resourcefileuri/)() const | Obtient ou définit l'identifiant uniforme de ressource (URI) utilisé pour référencer le fichier de ressource depuis le document. |
| [get_ResourceStream](./get_resourcestream/)() const | Permet de spécifier le flux où la ressource sera enregistrée. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_KeepResourceStreamOpen](./set_keepresourcestreamopen/)(bool) | Définisseur pour [Aspose::Words::Saving::ResourceSavingArgs::get_KeepResourceStreamOpen](./get_keepresourcestreamopen/). |
| [set_ResourceFileName](./set_resourcefilename/)(const System::String\&) | Définisseur pour [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName](./get_resourcefilename/). |
| [set_ResourceFileUri](./set_resourcefileuri/)(const System::String\&) | Définisseur pour [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri](./get_resourcefileuri/). |
| [set_ResourceStream](./set_resourcestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Définisseur pour [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream](./get_resourcestream/). |
| [set_ResourceStream](./set_resourcestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Remarques


Par défaut, lorsque Aspose.Words enregistre un document au format HTML, SVG ou Markdown à pages fixes, il enregistre chaque ressource dans un fichier séparé. Aspose.Words utilise le nom de fichier du document et un numéro unique pour générer un nom de fichier unique pour chaque ressource trouvée dans le document.

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

Pour appliquer votre propre logique de génération des noms de fichiers de ressources, utilisez la propriété [ResourceFileName](./get_resourcefilename/).

Pour enregistrer les ressources dans des flux au lieu de fichiers, utilisez la propriété [ResourceStream](./get_resourcestream/).
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
