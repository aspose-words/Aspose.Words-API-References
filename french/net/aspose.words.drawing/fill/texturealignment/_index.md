---
title: Fill.TextureAlignment
second_title: Référence de l'API Aspose.Words pour .NET
description: Fill propriété. Obtient ou définit lalignement pour le remplissage de la texture des carreaux.
type: docs
weight: 190
url: /fr/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Obtient ou définit l'alignement pour le remplissage de la texture des carreaux.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

### Exemples

Montre comment remplir et recouvrir la texture à l’intérieur de la forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Applique l'alignement de la texture au remplissage de la forme.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Utilisez l'option de conformité pour définir la forme en utilisant DML si vous souhaitez obtenir "TextureAlignment"
// propriété après l'enregistrement du document.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### Voir également

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../fill/)
* Assemblée [Aspose.Words](../../../)


