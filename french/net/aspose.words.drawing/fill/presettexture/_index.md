---
title: Fill.PresetTexture
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words pour .NET
description: Découvrez comment configurer facilement la propriété PresetTexture et sublimer vos créations avec de superbes options de remplissage. Libérez votre potentiel créatif dès aujourd'hui !
type: docs
weight: 170
url: /fr/net/aspose.words.drawing/fill/presettexture/
---
## Fill.PresetTexture property

Obtient un[`PresetTexture`](../../presettexture/) pour le remplissage.

```csharp
public PresetTexture PresetTexture { get; }
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

* enum [PresetTexture](../../presettexture/)
* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
