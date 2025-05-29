---
title: ShapeBase.RelativeVerticalPosition
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase RelativeVerticalPosition pour améliorer l'alignement vertical des formes, garantissant un contrôle précis de la mise en page dans vos conceptions.
type: docs
weight: 470
url: /fr/net/aspose.words.drawing/shapebase/relativeverticalposition/
---
## ShapeBase.RelativeVerticalPosition property

Spécifie par rapport à quoi la forme est positionnée verticalement.

```csharp
public RelativeVerticalPosition RelativeVerticalPosition { get; set; }
```

## Remarques

La valeur par défaut estParagraph.

N'a d'effet que pour les formes flottantes de niveau supérieur.

## Exemples

Montre comment insérer une image flottante au centre d'une page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez une image flottante qui apparaîtra derrière le texte superposé et alignez-la au centre de la page.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Voir également

* enum [RelativeVerticalPosition](../../relativeverticalposition/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
