---
title: ShapeBase.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase VerticalAlignment pour optimiser le positionnement vertical de votre forme pour une précision de conception et un attrait visuel améliorés.
type: docs
weight: 600
url: /fr/net/aspose.words.drawing/shapebase/verticalalignment/
---
## ShapeBase.VerticalAlignment property

Spécifie comment la forme est positionnée verticalement.

```csharp
public VerticalAlignment VerticalAlignment { get; set; }
```

## Remarques

La valeur par défaut estNone.

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

* enum [VerticalAlignment](../../verticalalignment/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
