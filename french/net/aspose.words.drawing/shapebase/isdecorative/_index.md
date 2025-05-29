---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words pour .NET
description: Découvrez ShapeBase. Gérez facilement les propriétés décoratives de vos documents. Améliorez l'attrait visuel en définissant des indicateurs pour des formes uniques.
type: docs
weight: 260
url: /fr/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Obtient ou définit l'indicateur qui spécifie si la forme est décorative dans le document.

```csharp
public bool IsDecorative { get; set; }
```

## Remarques

Notez que la forme n'est pas vide[`AlternativeText`](../alternativetext/) ne peut pas être décoratif.

## Exemples

Montre comment définir que la forme est décorative.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// Si « AlternativeText » n'est pas vide, la forme ne peut pas être décorative.
// C'est pourquoi notre valeur est passée à « false ».
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// Créez une nouvelle forme décorative.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
