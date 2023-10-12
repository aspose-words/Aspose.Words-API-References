---
title: ShapeBase.IsDecorative
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Obtient ou définit lindicateur qui spécifie si la forme est décorative dans le document.
type: docs
weight: 240
url: /fr/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Obtient ou définit l'indicateur qui spécifie si la forme est décorative dans le document.

```csharp
public bool IsDecorative { get; set; }
```

### Remarques

Notez que la forme n'est pas vide[`AlternativeText`](../alternativetext/) ne peut pas être décoratif.

### Exemples

Montre comment définir que la forme est décorative.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape) doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// Si "AlternativeText" n'est pas vide, la forme ne peut pas être décorative.
// C'est pourquoi notre valeur est devenue « false ».
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// Crée une nouvelle forme décorative.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)


