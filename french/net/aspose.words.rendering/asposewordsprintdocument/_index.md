---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words pour .NET
description: Aspose.Words.Rendering.AsposeWordsPrintDocument classe. Fournit une implémentation par défaut pour limpression dunDocument au sein du framework dimpression .NET en C#.
type: docs
weight: 4530
url: /fr/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Fournit une implémentation par défaut pour l'impression d'un[`Document`](../../aspose.words/document/) au sein du framework d'impression .NET.

Pour en savoir plus, visitez le[Impression d'un document par programme ou à l'aide de boîtes de dialogue](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) article documentaire.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | Initialise une nouvelle instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Obtient ou définit la façon dont les pages non colorées sont imprimées si le périphérique prend en charge l'impression couleur. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Obtient le nombre de pages imprimées en couleur (c'est-à-dire avecColor défini sur vrai). |

## Méthodes

| Nom | La description |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Lit et met en cache certains champs dePrinterSettings pour réduire le temps d'impression. |

## Remarques

`AsposeWordsPrintDocument` remplacementsPrintEventArgs) pour imprimer la plage de pages spécifiée dansPrinterSettings.

Un seul document Word peut être composé de plusieurs sections qui spécifient des pages avec différentes tailles, orientations et bacs à papier.`AsposeWordsPrintDocument` overrides QueryPageSettingsEventArgs) pour sélectionner correctement le format de papier, l'orientation et la source de papier lors de l'impression d'un document Word.

Microsoft Word stocke les valeurs spécifiques à l'imprimante pour les bacs à papier dans un document Word et, par conséquent, , l'impression uniquement sur le même modèle d'imprimante que celui qui a été sélectionné lorsque l'utilisateur a spécifié les bacs à papier entraînera l'impression à partir des bacs appropriés. Si vous imprimez un document sur une autre imprimante, alors très probablement le bac à papier par défaut sera utilisé, et non les bacs spécifiés dans le document.

### Voir également

* espace de noms [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../)
