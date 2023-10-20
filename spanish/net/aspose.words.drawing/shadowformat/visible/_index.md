---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: Aspose.Words para .NET
description: ShadowFormat Visible propiedad. Devolucionesverdadero si el formato aplicado a esta instancia es visible en C#.
type: docs
weight: 20
url: /es/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Devoluciones`verdadero` si el formato aplicado a esta instancia es visible.

```csharp
public bool Visible { get; }
```

## Observaciones

A diferencia[`Clear`](../clear/) , asignando`FALSO` a Visible no borra el formato, solo oculta el efecto de forma.

## Ejemplos

Muestra cómo trabajar con un formato de sombra para la forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### Ver también

* class [ShadowFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
