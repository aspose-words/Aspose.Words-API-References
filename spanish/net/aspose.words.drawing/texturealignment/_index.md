---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.TextureAlignment para una alineación precisa del relleno de textura. ¡Mejore el diseño de sus documentos con opciones de mosaico uniformes!
type: docs
weight: 1780
url: /es/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Especifica la alineación para el mosaico del relleno de textura.

```csharp
public enum TextureAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| TopLeft | `0` | Alineación de textura superior izquierda. |
| Top | `1` | Alineación de textura superior. |
| TopRight | `2` | Alineación de textura superior derecha. |
| Left | `3` | Alineación de textura a la izquierda. |
| Center | `4` | Alineación de textura central. |
| Right | `5` | Alineación de textura a la derecha. |
| BottomLeft | `6` | Alineación de textura inferior izquierda. |
| Bottom | `7` | Alineación de la textura inferior. |
| BottomRight | `8` | Alineación de textura inferior derecha. |
| None | `9` | Ninguna alineación de textura. |

## Ejemplos

Muestra cómo rellenar y colocar en mosaico la textura dentro de la forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Aplicar alineación de textura al relleno de forma.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Utilice la opción de cumplimiento para definir la forma usando DML si desea obtener "TextureAlignment"
// propiedad después de guardar el documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);

doc = new Document(ArtifactsDir + "Shape.TextureFill.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(TextureAlignment.TopRight, shape.Fill.TextureAlignment);
Assert.AreEqual(PresetTexture.Canvas, shape.Fill.PresetTexture);
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
