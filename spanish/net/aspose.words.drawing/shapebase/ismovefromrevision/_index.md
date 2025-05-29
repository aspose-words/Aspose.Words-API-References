---
title: ShapeBase.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase IsMoveFromRevision en Microsoft Word. Realice un seguimiento de los cambios fácilmente e identifique con precisión los objetos movidos o eliminados.
type: docs
weight: 340
url: /es/net/aspose.words.drawing/shapebase/ismovefromrevision/
---
## ShapeBase.IsMoveFromRevision property

Devuelve`verdadero` Si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```csharp
public bool IsMoveFromRevision { get; }
```

## Ejemplos

Muestra cómo identificar formas de revisión de movimiento.

```csharp
// Una revisión de movimiento es cuando movemos un elemento en el cuerpo del documento cortándolo y pegándolo en Microsoft Word mientras
Seguimiento de cambios. Si se utiliza una forma en línea en dicho movimiento de texto, dicha forma también será una revisión.
// Copiar y pegar o mover formas flotantes no crea revisiones de movimiento.
Document doc = new Document(MyDir + "Revision shape.docx");

Las revisiones de movimiento consisten en pares de revisiones "Desde" y "A". Nos movimos en este documento con una forma,
// pero hasta que aceptemos o rechacemos la revisión del movimiento, habrá dos instancias de esa forma.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Esta es la revisión "Mover a", que es la forma en su destino de llegada.
// Si aceptamos la revisión, esta forma de revisión "Mover a" desaparecerá,
// y la forma de revisión "Mover desde" permanecerá.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Esta es la revisión "Mover desde", que es la forma en su ubicación original.
// Si aceptamos la revisión, esta forma de revisión "Mover desde" desaparecerá,
// y la forma de revisión "Mover a" permanecerá.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
