---
title: ShapeBase.BehindText
linktitle: BehindText
articleTitle: BehindText
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase BehindText pour contrôler la superposition des formes dans vos conceptions, améliorant ainsi la visibilité du texte et la précision de la mise en page sans effort.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

Spécifie si la forme est en dessous ou au-dessus du texte.

```csharp
public bool BehindText { get; set; }
```

## Remarques

N'a d'effet que sur les formes de niveau supérieur.

La valeur par défaut est`FAUX`.

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

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
