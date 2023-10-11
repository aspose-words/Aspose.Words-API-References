---
title: ShapeBase.RelativeHorizontalPosition
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Spécifie par rapport à quoi la forme est positionnée horizontalement.
type: docs
weight: 420
url: /fr/net/aspose.words.drawing/shapebase/relativehorizontalposition/
---
## ShapeBase.RelativeHorizontalPosition property

Spécifie par rapport à quoi la forme est positionnée horizontalement.

```csharp
public RelativeHorizontalPosition RelativeHorizontalPosition { get; set; }
```

### Remarques

La valeur par défaut estColumn.

N'a d'effet que sur les formes flottantes de niveau supérieur.

### Exemples

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

* enum [RelativeHorizontalPosition](../../relativehorizontalposition/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)


