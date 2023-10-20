---
title: ShapeBase.HorizontalAlignment
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words pour .NET
description: ShapeBase HorizontalAlignment propriété. Spécifie comment la forme est positionnée horizontalement en C#.
type: docs
weight: 220
url: /fr/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

Spécifie comment la forme est positionnée horizontalement.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

## Remarques

La valeur par défaut estNone.

N'a d'effet que sur les formes flottantes de niveau supérieur.

## Exemples

Montre comment insérer une image flottante au centre d’une page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une image flottante qui apparaîtra derrière le texte superposé et alignez-la au centre de la page.
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

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
