---
title: RevisionOptions.InsertCellColor
linktitle: InsertCellColor
articleTitle: InsertCellColor
second_title: Aspose.Words pour .NET
description: Personnalisez votre feuille de calcul avec la propriété InsertCellColor dans RevisionOptions. Choisissez la couleur des cellules insérées ; la couleur par défaut est le bleu !
type: docs
weight: 50
url: /fr/net/aspose.words.layout/revisionoptions/insertcellcolor/
---
## RevisionOptions.InsertCellColor property

Permet de spécifier la couleur à utiliser pour les cellules inséréesInsertion . La valeur par défaut estBlue .

```csharp
public RevisionColor InsertCellColor { get; set; }
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
