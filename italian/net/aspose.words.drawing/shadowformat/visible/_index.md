---
title: ShadowFormat.Visible
second_title: Aspose.Words per .NET API Reference
description: ShadowFormat proprietà. RestituisceVERO se la formattazione applicata a questa istanza è visibile.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Restituisce`VERO` se la formattazione applicata a questa istanza è visibile.

```csharp
public bool Visible { get; }
```

### Osservazioni

A differenza[`Clear`](../clear/) , assegnando`falso` a Visibile non cancella la formattazione, nasconde solo l'effetto forma.

### Esempi

Mostra come utilizzare la formattazione dell'ombra per la forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### Guarda anche

* class [ShadowFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shadowformat/)
* assemblea [Aspose.Words](../../../)


