---
title: ShapeBase.IsTopLevel
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. RestituisceVEROse questa forma non è figlia di una forma di gruppo.
type: docs
weight: 350
url: /it/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Restituisce`VERO`se questa forma non è figlia di una forma di gruppo.

```csharp
public bool IsTopLevel { get; }
```

### Esempi

Mostra come determinare se una forma fa parte di una forma di gruppo.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// Una forma per impostazione predefinita non fa parte di alcuna forma di gruppo e pertanto ha la proprietà "IsTopLevel" impostata su "true".
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// Una volta assimilata una forma in una forma di gruppo, la proprietà "IsTopLevel" cambia in "false".
Assert.False(shape.IsTopLevel);
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


