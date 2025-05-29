---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase AnchorLocked pour contrôler le verrouillage de l'ancrage des formes, améliorant ainsi la stabilité et la flexibilité de la conception de vos projets.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

Spécifie si l'ancre de la forme est verrouillée.

```csharp
public bool AnchorLocked { get; set; }
```

## Remarques

La valeur par défaut est`FAUX`.

N'a d'effet que sur les formes de niveau supérieur.

Cette propriété affecte le comportement de l'ancre de la forme dans Microsoft Word. Lorsque l'ancre n'est pas verrouillée, le déplacement de la forme dans Microsoft Word peut également déplacer l'ancre de la forme.

## Exemples

Montre comment verrouiller ou déverrouiller l'ancre de paragraphe d'une forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// Définissez la propriété « AnchorLocked » sur « true » pour empêcher l'ancrage de la forme
// du déplacement lors du déplacement de la forme dans Microsoft Word.
// Définissez la propriété « AnchorLocked » sur « false » pour autoriser tout mouvement de la forme
// pour déplacer également son ancre vers tout autre paragraphe dont la forme se trouve à proximité.
shape.AnchorLocked = anchorLocked;

// Si la forme n'a pas de symbole d'ancrage visible à sa gauche,
// nous devrons activer les ancres visibles via "Options" -> "Affichage" -> "Ancres d'objet".
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
