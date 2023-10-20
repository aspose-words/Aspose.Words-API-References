---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: Aspose.Words para .NET
description: ShapeBase AlternativeText propiedad. Define texto alternativo que se mostrará en lugar de un gráfico en C#.
type: docs
weight: 20
url: /es/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

Define texto alternativo que se mostrará en lugar de un gráfico.

```csharp
public string AlternativeText { get; set; }
```

## Observaciones

El valor predeterminado es una cadena vacía.

## Ejemplos

Muestra cómo utilizar el texto alternativo de una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Podemos acceder al texto alternativo de una forma haciendo clic derecho sobre ella y luego mediante "Formato de autoforma" -> "Texto alternativo".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Guarde el documento en HTML y luego elimine la imagen vinculada que pertenece a nuestra forma.
// El navegador que lee nuestro HTML mostrará el texto alternativo en lugar de la imagen que falta.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
