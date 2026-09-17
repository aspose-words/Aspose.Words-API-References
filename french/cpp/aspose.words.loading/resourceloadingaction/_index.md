---
title: "Aspose::Words::Loading::ResourceLoadingAction enum"
linktitle: "ResourceLoadingAction"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::ResourceLoadingAction enum. Spécifie le mode de chargement des ressources. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enum


Spécifie le mode de chargement des ressources. Pour en savoir plus, consultez l'article de documentation [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
enum class ResourceLoadingAction
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Default | 0 | Aspose.Words chargera cette ressource comme d'habitude. |
| Ignorer | 1 | Aspose.Words ignorera le chargement de cette ressource. Seul le lien sans données sera stocké pour une image, la feuille de style CSS sera ignorée pour le format HTML. |
| UserProvided | 2 | Aspose.Words utilisera le tableau d'octets fourni par l'utilisateur dans [SetData()](../) comme données de la ressource. |

## Voir aussi

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
