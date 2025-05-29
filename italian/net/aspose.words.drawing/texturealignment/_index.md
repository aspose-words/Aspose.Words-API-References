---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.TextureAlignment per un allineamento preciso del riempimento delle texture. Migliora la progettazione dei tuoi documenti con opzioni di affiancamento senza soluzione di continuità!
type: docs
weight: 1780
url: /it/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Specifica l'allineamento per la piastrellatura del riempimento della texture.

```csharp
public enum TextureAlignment
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| TopLeft | `0` | Allineamento della texture in alto a sinistra. |
| Top | `1` | Allineamento della trama superiore. |
| TopRight | `2` | Allineamento della texture in alto a destra. |
| Left | `3` | Allineamento texture a sinistra. |
| Center | `4` | Allineamento della texture al centro. |
| Right | `5` | Allineamento texture corretto. |
| BottomLeft | `6` | Allineamento della texture in basso a sinistra. |
| Bottom | `7` | Allineamento della trama inferiore. |
| BottomRight | `8` | Allineamento della texture in basso a destra. |
| None | `9` | Nessun allineamento della texture. |

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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
