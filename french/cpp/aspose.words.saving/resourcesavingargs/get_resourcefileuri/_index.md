---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri méthode"
linktitle: "get_ResourceFileUri"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri méthode. Obtient ou définit l'identifiant uniforme de ressource (URI) utilisé pour référencer le fichier de ressource depuis le document en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/resourcesavingargs/get_resourcefileuri/
---
## ResourceSavingArgs::get_ResourceFileUri method


Obtient ou définit l'identifiant uniforme de ressource (URI) utilisé pour référencer le fichier de ressource depuis le document.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri() const
```

## Remarques


Cette propriété vous permet de modifier les URI des fichiers de ressources exportés vers des documents HTML à page fixe, SVG ou Markdown.

Aspose.Words génère automatiquement un URI pour chaque fichier de ressource lors de l'exportation au format HTML à page fixe, SVG ou Markdown. Les URI générés font référence aux fichiers de ressources enregistrés par Aspose.Words. Cependant, les URI peuvent être incorrects si les fichiers de ressources sont déplacés vers un autre emplacement ou si les fichiers de ressources sont enregistrés dans des flux. Cette propriété permet de corriger les URI dans ces cas.

Lorsque l'événement est déclenché, cette propriété contient le URI généré par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour fournir un URI personnalisé pour le fichier de ressource.
## Voir aussi

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
