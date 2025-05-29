---
title: ShapeBase.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words per .NET
description: Controlla la visibilità delle forme con la proprietà nascosta di ShapeBase. Passa facilmente da visibile a nascosto per una maggiore flessibilità di progettazione.
type: docs
weight: 230
url: /it/net/aspose.words.drawing/shapebase/hidden/
---
## ShapeBase.Hidden property

Ottiene o imposta un valore booleano che indica se la forma è visibile.

```csharp
public bool Hidden { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` .

## Esempi

Mostra come nascondere la forma.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
if (!shape.Hidden)
    shape.Hidden = true;

doc.Save(ArtifactsDir + "Shape.Hidden.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
