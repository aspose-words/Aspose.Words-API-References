---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase AlternativeText, qui améliore l'accessibilité en fournissant un texte descriptif pour les graphiques, améliorant ainsi l'expérience utilisateur et le référencement.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

Définit un texte alternatif à afficher à la place d'un graphique.

```csharp
public string AlternativeText { get; set; }
```

## Remarques

La valeur par défaut est une chaîne vide.

## Exemples

Montre comment utiliser le texte alternatif d'une forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Nous pouvons accéder au texte alternatif d'une forme en cliquant dessus avec le bouton droit de la souris, puis via « Format de la forme automatique » -> « Texte alternatif ».
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Enregistrez le document au format HTML, puis supprimez l'image liée qui appartient à notre forme.
// Le navigateur qui lit notre HTML affichera le texte alternatif à la place de l'image manquante.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
