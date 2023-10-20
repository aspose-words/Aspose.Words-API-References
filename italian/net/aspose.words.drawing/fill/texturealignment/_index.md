---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words per .NET
description: Fill TextureAlignment proprietà. Ottiene o imposta lallineamento per il riempimento della texture delle tessere in C#.
type: docs
weight: 180
url: /it/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Ottiene o imposta l'allineamento per il riempimento della texture delle tessere.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

## Esempi

Mostra come riempire e affiancare la texture all'interno della forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Applica l'allineamento della trama al riempimento della forma.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Utilizza l'opzione di conformità per definire la forma utilizzando DML se desideri ottenere "TextureAlignment"
// proprietà dopo il salvataggio del documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### Guarda anche

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
