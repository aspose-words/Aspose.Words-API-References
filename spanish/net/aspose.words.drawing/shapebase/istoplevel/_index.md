---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: Aspose.Words para .NET
description: Descubre ShapeBase IsTopLevel. Comprueba rápidamente si una forma es independiente, optimizando tu flujo de trabajo de diseño con una gestión eficiente de grupos.
type: docs
weight: 370
url: /es/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Devuelve`verdadero` si esta forma no es hija de un grupo shape.

```csharp
public bool IsTopLevel { get; }
```

## Ejemplos

Muestra cómo determinar si una forma es parte de un grupo de formas.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// Una forma por defecto no es parte de ningún grupo de formas y por lo tanto tiene la propiedad "IsTopLevel" establecida en "verdadero".
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// Una vez que asimilamos una forma a una forma de grupo, la propiedad "IsTopLevel" cambia a "falso".
Assert.False(shape.IsTopLevel);
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
