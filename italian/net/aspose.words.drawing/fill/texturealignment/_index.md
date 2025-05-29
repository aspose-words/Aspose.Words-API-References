---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words per .NET
description: Imposta la proprietà TextureAlignment per ottimizzare il riempimento della texture delle tile. Personalizza facilmente l'allineamento per un impatto visivo migliore e una maggiore precisione nel design.
type: docs
weight: 190
url: /it/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Ottiene o imposta l'allineamento per il riempimento della trama delle piastrelle.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

## Esempi

Mostra come riempire e piastrellare la texture all'interno della forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Applica l'allineamento della texture al riempimento della forma.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Utilizzare l'opzione di conformità per definire la forma utilizzando DML se si desidera ottenere "TextureAlignment"
// proprietà dopo il salvataggio del documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);

doc = new Document(ArtifactsDir + "Shape.TextureFill.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(TextureAlignment.TopRight, shape.Fill.TextureAlignment);
Assert.AreEqual(PresetTexture.Canvas, shape.Fill.PresetTexture);
```

### Guarda anche

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
