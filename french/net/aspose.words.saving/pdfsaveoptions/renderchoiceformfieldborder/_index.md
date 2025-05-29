---
title: PdfSaveOptions.RenderChoiceFormFieldBorder
linktitle: RenderChoiceFormFieldBorder
articleTitle: RenderChoiceFormFieldBorder
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété PdfSaveOptions RenderChoiceFormFieldBorder améliore la conception des formulaires PDF en contrôlant les bordures des champs de choix pour une meilleure expérience utilisateur.
type: docs
weight: 290
url: /fr/net/aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/
---
## PdfSaveOptions.RenderChoiceFormFieldBorder property

Spécifie s'il faut restituer la bordure du champ de formulaire de choix PDF.

```csharp
public bool RenderChoiceFormFieldBorder { get; set; }
```

## Remarques

Les champs de formulaire de choix PDF sont utilisés pour l'exportation du contrôle de contenu de la zone de liste déroulante SDT, du contrôle de contenu de la liste déroulante SDT et du champ de formulaire déroulant hérité lorsque[`PreserveFormFields`](../preserveformfields/) l'option est activée.

La valeur par défaut est`vrai`.

## Exemples

Montre comment rendre la bordure du champ de formulaire de choix PDF.

```csharp
Document doc = new Document(MyDir + "Legacy drop-down.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
saveOptions.RenderChoiceFormFieldBorder = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderChoiceFormFieldBorder.pdf", saveOptions);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
