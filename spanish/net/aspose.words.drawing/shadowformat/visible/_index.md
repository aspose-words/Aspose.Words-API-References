---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShadowFormat Visible. Compruebe fácilmente si su formato es visible, mejorando así la apariencia y la claridad de su documento.
type: docs
weight: 30
url: /es/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Devuelve`verdadero` si el formato aplicado a esta instancia es visible.

```csharp
public bool Visible { get; }
```

## Observaciones

A diferencia de[`Clear`](../clear/) , asignando`FALSO`Visible no borra el formato, solo oculta el efecto de forma.

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
