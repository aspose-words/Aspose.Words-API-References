---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase AnchorLocked para controlar el bloqueo de anclajes para formas, mejorando la estabilidad del diseño y la flexibilidad en sus proyectos.
type: docs
weight: 30
url: /es/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

Especifica si el ancla de la forma está bloqueada.

```csharp
public bool AnchorLocked { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO`.

Tiene efecto sólo para formas de nivel superior.

Esta propiedad afecta el comportamiento del ancla de la forma en Microsoft Word. Cuando el ancla no está bloqueado, al mover la forma en Microsoft Word también se puede mover el ancla de la forma.

## Ejemplos

Muestra cómo bloquear o desbloquear el ancla de párrafo de una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// Establezca la propiedad "AnchorLocked" en "verdadero" para evitar el anclaje de la forma
// de moverse al mover la forma en Microsoft Word.
// Establezca la propiedad "AnchorLocked" en "falso" para permitir cualquier movimiento de la forma
// para mover también su ancla a cualquier otro párrafo cerca del cual la forma termine.
shape.AnchorLocked = anchorLocked;

// Si la forma no tiene un símbolo de ancla visible a su izquierda,
// necesitaremos habilitar los anclajes visibles a través de "Opciones" -> "Mostrar" -> "Anclajes de objeto".
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
