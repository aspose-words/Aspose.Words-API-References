---
title: ShapeBase.VerticalAlignment
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Spécifie comment la forme est positionnée verticalement.
type: docs
weight: 510
url: /fr/net/aspose.words.drawing/shapebase/verticalalignment/
---
## ShapeBase.VerticalAlignment property

Spécifie comment la forme est positionnée verticalement.

```csharp
public VerticalAlignment VerticalAlignment { get; set; }
```

### Remarques

La valeur par défaut estNone.

N'a d'effet que pour les formes flottantes de niveau supérieur.

### Exemples

Montre comment insérer une image flottante au centre d'une page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une image flottante qui apparaîtra derrière le texte superposé et l'aligne au centre de la page.
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
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)


