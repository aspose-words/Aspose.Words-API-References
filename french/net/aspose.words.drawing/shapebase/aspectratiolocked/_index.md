---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words pour .NET
description: ShapeBase AspectRatioLocked propriété. Spécifie si les proportions de la forme sont verrouillées en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

Spécifie si les proportions de la forme sont verrouillées.

```csharp
public bool AspectRatioLocked { get; set; }
```

## Remarques

La valeur par défaut dépend du[`ShapeType`](../../shapetype/) , pour leImage c'est`vrai` mais pour les autres types de forme, c'est le cas`FAUX`.

A un effet uniquement sur les formes de niveau supérieur.

## Exemples

Montre comment verrouiller/déverrouiller les proportions d’une forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une forme. Si nous ouvrons ce document dans Microsoft Word, nous pouvons cliquer avec le bouton gauche sur la forme pour révéler
// huit poignées de redimensionnement autour de son périmètre, sur lesquelles nous pouvons cliquer et faire glisser pour modifier sa taille.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Définissez la propriété "AspectRatioLocked" sur "true" pour préserver les proportions de la forme
// lors de l'utilisation de l'une des quatre poignées de redimensionnement diagonales, qui modifient à la fois la hauteur et la largeur de l'image.
// L'utilisation de poignées de dimensionnement orthogonales qui modifient la hauteur ou la largeur modifiera toujours le rapport hauteur/largeur.
// Fixe la propriété "AspectRatioLocked" à "false" pour nous permettre de
// modifie librement le rapport hauteur/largeur de l'image avec toutes les poignées de dimensionnement.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
