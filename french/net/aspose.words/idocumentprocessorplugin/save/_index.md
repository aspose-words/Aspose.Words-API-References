---
title: IDocumentProcessorPlugin.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words pour .NET
description: Enregistrez vos documents sans effort avec la méthode d'enregistrement IDocumentProcessorPlugin, garantissant une sortie optimale avec des options d'enregistrement personnalisables selon vos besoins.
type: docs
weight: 30
url: /fr/net/aspose.words/idocumentprocessorplugin/save/
---
## IDocumentProcessorPlugin.Save method

Enregistrer le document chargé par[`Load`](../load/) méthode vers le flux de sortie en utilisant les options de sauvegarde spécifiées.

```csharp
public void Save(Stream outputStream, SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| outputStream | Stream | Le flux de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |

## Remarques

Si le format de sortie spécifié est image, seule l'image de la première page est enregistrée dans le flux de sortie. Si le format d'enregistrement spécifié n'est pas pris en charge nativement par le plugin (nécessite un chargement sur[`Document`](../../document/)), la méthode génère une exception.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* interface [IDocumentProcessorPlugin](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
