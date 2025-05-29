---
title: ReflectionFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words para .NET
description: Elimine sin esfuerzo ReflectionFormat de su objeto principal con nuestro método Remove optimizado, mejorando la eficiencia y la claridad de su codificación.
type: docs
weight: 50
url: /es/net/aspose.words.drawing/reflectionformat/remove/
---
## ReflectionFormat.Remove method

Elimina[`ReflectionFormat`](../) del objeto padre.

```csharp
public void Remove()
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
