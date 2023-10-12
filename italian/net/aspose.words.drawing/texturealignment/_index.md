---
title: Enum TextureAlignment
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.TextureAlignment enum. Specifica lallineamento per laffiancamento del riempimento texture.
type: docs
weight: 1370
url: /it/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Specifica l'allineamento per l'affiancamento del riempimento texture.

```csharp
public enum TextureAlignment
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| TopLeft | `0` | Allineamento texture in alto a sinistra. |
| Top | `1` | Allineamento texture superiore. |
| TopRight | `2` | Allineamento texture in alto a destra. |
| Left | `3` | Allineamento texture a sinistra. |
| Center | `4` | Allineamento texture centrale. |
| Right | `5` | Allineamento corretto della trama. |
| BottomLeft | `6` | Allineamento texture in basso a sinistra. |
| Bottom | `7` | Allineamento texture inferiore. |
| BottomRight | `8` | Allineamento texture in basso a destra. |
| None | `9` | Nessuno allineamento texture. |

### Esempi

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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)


