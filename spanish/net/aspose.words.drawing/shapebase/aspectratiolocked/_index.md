---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words para .NET
description: Descubre la propiedad ShapeBase AspectRatioLocked para mantener fácilmente la relación de aspecto de tus formas y lograr diseños perfectos. ¡Mejora tus proyectos hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

Especifica si la relación de aspecto de la forma está bloqueada.

```csharp
public bool AspectRatioLocked { get; set; }
```

## Observaciones

El valor predeterminado depende de la[`ShapeType`](../../shapetype/) , para elImage es`verdadero` pero para los otros tipos de forma es`FALSO`.

Tiene efecto sólo para formas de nivel superior.

## Ejemplos

Muestra cómo bloquear/desbloquear la relación de aspecto de una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar una forma. Si abrimos este documento en Microsoft Word, podemos hacer clic izquierdo en la forma para mostrarla.
//ocho controladores de tamaño alrededor de su perímetro, en los que podemos hacer clic y arrastrar para cambiar su tamaño.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Establezca la propiedad "AspectRatioLocked" en "verdadero" para preservar la relación de aspecto de la forma
// al utilizar cualquiera de los cuatro controladores de tamaño diagonales, que cambian tanto la altura como el ancho de la imagen.
// El uso de cualquier controlador de tamaño ortogonal que cambie la altura o el ancho seguirá cambiando la relación de aspecto.
// Establezca la propiedad "AspectRatioLocked" en "falso" para permitirnos
// cambia libremente la relación de aspecto de la imagen con todos los controladores de tamaño.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
