---
title: ShapeBase.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase SizeInPoints pour récupérer et gérer facilement les dimensions de forme en points pour un contrôle de conception précis.
type: docs
weight: 540
url: /fr/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

Obtient la taille de la forme en points.

```csharp
public SizeF SizeInPoints { get; }
```

## Exemples

Montre comment vérifier la taille et le langage de balisage d'une forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
