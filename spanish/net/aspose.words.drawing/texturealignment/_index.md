---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.TextureAlignment enumeración. Especifica la alineación para el mosaico del relleno de textura en C#.
type: docs
weight: 1370
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
| Left | `3` | Alineación de textura izquierda. |
| Center | `4` | Alineación central de textura. |
| Right | `5` | Alineación de textura derecha. |
| BottomLeft | `6` | Alineación de textura inferior izquierda. |
| Bottom | `7` | Alineación de textura inferior. |
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
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
