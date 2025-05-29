---
title: Fill.PresetTexture
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words per .NET
description: Scopri come impostare la proprietà PresetTexture senza sforzo e migliorare i tuoi progetti con straordinarie opzioni di riempimento. Scatena il tuo potenziale creativo oggi stesso!
type: docs
weight: 170
url: /it/net/aspose.words.drawing/fill/presettexture/
---
## Fill.PresetTexture property

Ottiene un[`PresetTexture`](../../presettexture/) per il riempimento.

```csharp
public PresetTexture PresetTexture { get; }
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

* enum [PresetTexture](../../presettexture/)
* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
