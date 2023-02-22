---
title: Fill.TextureAlignment
second_title: Referencia de API de Aspose.Words para .NET
description: Fill propiedad. Obtiene o establece la alineación para el relleno de textura de mosaico.
type: docs
weight: 130
url: /es/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Obtiene o establece la alineación para el relleno de textura de mosaico.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

### Ejemplos

Muestra cómo rellenar y colocar en mosaico la textura dentro de la forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Aplicar alineación de textura al relleno de forma.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Use la opción de cumplimiento para definir la forma usando DML si desea obtener "TextureAlignment"
// propiedad después de guardar el documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### Ver también

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../fill/)
* asamblea [Aspose.Words](../../../)


