---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words pour .NET
description: Définissez la propriété TextureAlignment pour optimiser le remplissage de la texture des tuiles. Personnalisez facilement l'alignement pour un attrait visuel et une précision de conception accrus.
type: docs
weight: 190
url: /fr/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Obtient ou définit l'alignement pour le remplissage de la texture des tuiles.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

## Exemples

Montre comment remplir et carreler la texture à l'intérieur de la forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Appliquer l'alignement de la texture au remplissage de la forme.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Utilisez l'option de conformité pour définir la forme à l'aide de DML si vous souhaitez obtenir « TextureAlignment »
// propriété après l'enregistrement du document.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);

doc = new Document(ArtifactsDir + "Shape.TextureFill.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(TextureAlignment.TopRight, shape.Fill.TextureAlignment);
Assert.AreEqual(PresetTexture.Canvas, shape.Fill.PresetTexture);
```

### Voir également

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
