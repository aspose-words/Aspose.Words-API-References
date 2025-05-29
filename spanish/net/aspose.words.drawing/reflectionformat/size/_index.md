---
title: ReflectionFormat.Size
linktitle: Size
articleTitle: Size
second_title: Aspose.Words para .NET
description: Descubre la propiedad ReflectionFormat Size, que controla el tamaño del reflejo (0.0-1.0) para lograr efectos visuales impactantes en tus diseños. ¡Mejora la estética de tu proyecto!
type: docs
weight: 30
url: /es/net/aspose.words.drawing/reflectionformat/size/
---
## ReflectionFormat.Size property

Obtiene o establece un valor doble entre 0,0 y 1,0 que representa el tamaño del reflejo como un porcentaje del objeto reflejado. El valor predeterminado es 0,0.

```csharp
public double Size { get; set; }
```

## Ejemplos

Muestra cómo interactuar con el efecto de forma de reflexión.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Reflection.Transparency = 0.37;
shape.Reflection.Size = 0.48;
shape.Reflection.Blur = 17.5;
shape.Reflection.Distance = 9.2;

doc.Save(ArtifactsDir + "Shape.Reflection.docx");

doc = new Document(ArtifactsDir + "Shape.Reflection.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ReflectionFormat reflectionFormat = shape.Reflection;

Assert.AreEqual(0.37d, reflectionFormat.Transparency, 0.01d);
Assert.AreEqual(0.48d, reflectionFormat.Size, 0.01d);
Assert.AreEqual(17.5d, reflectionFormat.Blur, 0.01d);
Assert.AreEqual(9.2d, reflectionFormat.Distance, 0.01d);

reflectionFormat.Remove();

Assert.AreEqual(0, reflectionFormat.Transparency);
Assert.AreEqual(0, reflectionFormat.Size);
Assert.AreEqual(0, reflectionFormat.Blur);
Assert.AreEqual(0, reflectionFormat.Distance);
```

### Ver también

* class [ReflectionFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
