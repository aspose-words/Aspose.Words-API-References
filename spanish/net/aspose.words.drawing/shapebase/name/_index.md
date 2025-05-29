---
title: ShapeBase.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase Name para administrar fácilmente nombres de formas opcionales, mejorando la flexibilidad de su diseño y la organización del proyecto.
type: docs
weight: 420
url: /es/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Obtiene o establece el nombre de forma opcional.

```csharp
public string Name { get; set; }
```

## Observaciones

El valor predeterminado es una cadena vacía.

No puede ser`nulo`, pero puede ser una cadena vacía.

## Ejemplos

Muestra cómo utilizar el texto alternativo de una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

//Podemos acceder al texto alternativo de una forma haciendo clic derecho sobre ella y luego a través de "Formato de autoforma" -> "Texto alternativo".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Guarde el documento en HTML y luego elimine la imagen vinculada que pertenece a nuestra forma.
// El navegador que lee nuestro HTML mostrará el texto alternativo en lugar de la imagen faltante.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
