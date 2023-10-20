---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words pour .NET
description: FixedPageSaveOptions OptimizeOutput propriété. Lindicateur indique sil est nécessaire doptimiser la sortie. Si cet indicateur est défini les canevas imbriqués redondants et les canevas vides sont supprimés également les glyphes voisins avec le même formatage sont concaténés. Remarque  la précision de laffichage du contenu peut être affectée si cette propriété est définie survrai . La valeur par défaut estFAUX  en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

L'indicateur indique s'il est nécessaire d'optimiser la sortie. Si cet indicateur est défini, les canevas imbriqués redondants et les canevas vides sont supprimés, également les glyphes voisins avec le même formatage sont concaténés. Remarque : la précision de l'affichage du contenu peut être affectée si cette propriété est définie sur`vrai` . La valeur par défaut est`FAUX` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## Exemples

Montre comment optimiser les objets de document lors de l'enregistrement au format XP.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Crée un objet "XpsSaveOptions" à passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

// Définissez la propriété "OptimizeOutput" sur "true" pour prendre des mesures telles que la suppression des canevas imbriqués ou vides
// et concaténer les exécutions adjacentes avec un formatage identique pour optimiser le contenu du document de sortie.
// Cela peut affecter l'apparence du document.
// Définissez la propriété "OptimizeOutput" sur "false" pour enregistrer le document normalement.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Voir également

* class [FixedPageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
