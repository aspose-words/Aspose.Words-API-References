---
title: RevisionOptions.DeleteCellColor
linktitle: DeleteCellColor
articleTitle: DeleteCellColor
second_title: Aspose.Words pour .NET
description: Personnalisez votre feuille de calcul avec la propriété DeleteCellColor de RevisionOptions. Définissez facilement une couleur unique pour les cellules supprimées, améliorant ainsi la clarté et l'organisation.
type: docs
weight: 20
url: /fr/net/aspose.words.layout/revisionoptions/deletecellcolor/
---
## RevisionOptions.DeleteCellColor property

Permet de spécifier la couleur à utiliser pour les cellules suppriméesDeletion . La valeur par défaut estPink .

```csharp
public RevisionColor DeleteCellColor { get; set; }
```

## Exemples

Montre comment travailler avec la couleur de révision des cellules d'insertion/suppression.

```csharp
Document doc = new Document(MyDir + "Cell revisions.docx");

doc.LayoutOptions.RevisionOptions.InsertCellColor = RevisionColor.LightBlue;
doc.LayoutOptions.RevisionOptions.DeleteCellColor = RevisionColor.DarkRed;

doc.Save(ArtifactsDir + "Revision.RevisionCellColor.pdf");
```

### Voir également

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
