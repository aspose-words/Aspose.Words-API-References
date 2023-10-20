---
title: ShadowFormat.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words para .NET
description: ShadowFormat Clear método. Borra el formato de sombra en C#.
type: docs
weight: 30
url: /es/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Borra el formato de sombra.

```csharp
public void Clear()
```

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
