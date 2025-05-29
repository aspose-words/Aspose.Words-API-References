---
title: IDocumentProcessorPlugin Interface
linktitle: IDocumentProcessorPlugin
articleTitle: IDocumentProcessorPlugin
second_title: Aspose.Words pour .NET
description: Découvrez l'interface Aspose.Words IDocumentProcessorPlugin pour améliorer le traitement de vos documents avec de puissants plugins externes pour une intégration transparente.
type: docs
weight: 3610
url: /fr/net/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface

Définit une interface pour le plugin de traitement de documents externe.

```csharp
public interface IDocumentProcessorPlugin
```

## Méthodes

| Nom | La description |
| --- | --- |
| [Append](../../aspose.words/idocumentprocessorplugin/append/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Ajoutez le document en le chargeant avec les options de chargement spécifiées. |
| [Load](../../aspose.words/idocumentprocessorplugin/load/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Chargez le document en utilisant les options de chargement spécifiées. |
| [Save](../../aspose.words/idocumentprocessorplugin/save/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Enregistrer le document chargé par[`Load`](./load/) méthode vers le flux de sortie en utilisant les options de sauvegarde spécifiées. |
| [SetImageWatermark](../../aspose.words/idocumentprocessorplugin/setimagewatermark/)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Ajoute un filigrane d'image sur chaque page du document chargé par[`Load`](./load/) méthode. |
| [SetTextWatermark](../../aspose.words/idocumentprocessorplugin/settextwatermark/)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Ajoute un filigrane de texte sur chaque page du document chargé par[`Load`](./load/) méthode. |
| [ToDocument](../../aspose.words/idocumentprocessorplugin/todocument/)() | Analyse le document chargé par[`Load`](./load/) méthode dans[`Document`](../document/) objet. |
| [ToPages](../../aspose.words/idocumentprocessorplugin/topages/)(*[FixedPageSaveOptions](../../aspose.words.saving/fixedpagesaveoptions/)*) | Enregistre chaque page du document chargé par[`Load`](./load/) méthode utilisant les options d'enregistrement de page fixe spécifiées. |

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
