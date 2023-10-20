---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: Aspose.Words para .NET
description: ShapeBase IsTopLevel propiedad. Devolucionesverdaderosi esta forma no es hija de una forma de grupo en C#.
type: docs
weight: 350
url: /es/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Devoluciones`verdadero`si esta forma no es hija de una forma de grupo.

```csharp
public bool IsTopLevel { get; }
```

## Ejemplos

Muestra cómo saber si una forma es parte de una forma de grupo.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// Una forma por defecto no forma parte de ninguna forma de grupo y, por lo tanto, tiene la propiedad "IsTopLevel" establecida en "true".
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// Una vez que asimilamos una forma a una forma de grupo, la propiedad "IsTopLevel" cambia a "false".
Assert.False(shape.IsTopLevel);
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
