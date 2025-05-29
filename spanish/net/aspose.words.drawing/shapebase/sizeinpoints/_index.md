---
title: ShapeBase.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase SizeInPoints para recuperar y administrar fácilmente las dimensiones de forma en puntos para un control de diseño preciso.
type: docs
weight: 540
url: /es/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

Obtiene el tamaño de la forma en puntos.

```csharp
public SizeF SizeInPoints { get; }
```

## Ejemplos

Muestra cómo verificar el tamaño de una forma y el lenguaje de marcado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
