---
title: ReflectionFormat Class
linktitle: ReflectionFormat
articleTitle: ReflectionFormat
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.ReflectionFormat para el formato avanzado de reflexión de objetos. ¡Mejore el diseño de sus documentos con una integración perfecta!
type: docs
weight: 1570
url: /es/net/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class

Representa el formato de reflexión de un objeto.

```csharp
public class ReflectionFormat
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Blur](../../aspose.words.drawing/reflectionformat/blur/) { get; set; } | Obtiene o establece un valor doble que especifica el grado de efecto de desenfoque aplicado al efecto de reflejo en puntos. El valor predeterminado es 0.0. |
| [Distance](../../aspose.words.drawing/reflectionformat/distance/) { get; set; } | Obtiene o establece un valor doble que especifica la cantidad de separación de la imagen reflejada del objeto en puntos. El valor predeterminado es 0.0. |
| [Size](../../aspose.words.drawing/reflectionformat/size/) { get; set; } | Obtiene o establece un valor doble entre 0,0 y 1,0 que representa el tamaño del reflejo como un porcentaje del objeto reflejado. El valor predeterminado es 0,0. |
| [Transparency](../../aspose.words.drawing/reflectionformat/transparency/) { get; set; } | Obtiene o establece un valor doble entre 0.0 (opaco) y 1.0 (transparente) que representa el grado de transparencia para el efecto de reflejo. El valor predeterminado es 0.0. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Remove](../../aspose.words.drawing/reflectionformat/remove/)() | Elimina`ReflectionFormat` del objeto padre. |

## Observaciones

Utilice el[`Reflection`](../shapebase/reflection/) propiedad para acceder a las propiedades de reflexión de un objeto. No crea instancias de la`ReflectionFormat` clase directamente.

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

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
