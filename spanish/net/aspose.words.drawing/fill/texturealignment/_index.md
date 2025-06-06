---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words para .NET
description: Establezca la propiedad TextureAlignment para optimizar el relleno de textura de los mosaicos. Personalice fácilmente la alineación para mejorar el atractivo visual y la precisión del diseño.
type: docs
weight: 190
url: /es/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Obtiene o establece la alineación para el relleno de textura de mosaico.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

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

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
