---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: Aspose.Words per .NET
description: Scopri ShapeBase IsTopLevel. Verifica rapidamente se una forma è indipendente, migliorando il flusso di lavoro di progettazione con una gestione efficiente dei gruppi.
type: docs
weight: 370
url: /it/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Restituisce`VERO` se questa forma non è figlia di una forma di gruppo.

```csharp
public bool IsTopLevel { get; }
```

## Esempi

Mostra come stabilire se una forma fa parte di un gruppo di forme.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// Per impostazione predefinita, una forma non fa parte di alcun gruppo di forme e pertanto la proprietà "IsTopLevel" è impostata su "true".
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// Una volta che assimiliamo una forma in una forma di gruppo, la proprietà "IsTopLevel" cambia in "false".
Assert.False(shape.IsTopLevel);
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
