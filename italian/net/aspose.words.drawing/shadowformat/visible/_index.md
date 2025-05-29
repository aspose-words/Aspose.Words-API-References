---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShadowFormat Visible. Controlla facilmente se la formattazione è visibile, migliorando l'aspetto e la chiarezza del tuo documento.
type: docs
weight: 30
url: /it/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Restituisce`VERO` se la formattazione applicata a questa istanza è visibile.

```csharp
public bool Visible { get; }
```

## Osservazioni

A differenza di[`Clear`](../clear/) , assegnando`falso`su Visibile non cancella la formattazione, nasconde solo l'effetto forma.

## Esempi

Mostra come lavorare con una formattazione ombra per la forma.

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
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
