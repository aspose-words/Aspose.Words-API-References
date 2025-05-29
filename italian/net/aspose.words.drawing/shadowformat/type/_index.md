---
title: ShadowFormat.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Esplora la proprietà ShadowFormat Type per personalizzare facilmente gli effetti ombra. Ottieni o imposta ShadowType per una maggiore flessibilità di progettazione.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/shadowformat/type/
---
## ShadowFormat.Type property

Ottiene o imposta il valore specificato[`ShadowType`](../../shadowtype/) per ShadowFormat.

```csharp
public ShadowType Type { get; set; }
```

## Esempi

Mostra come ottenere il colore dell'ombra.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Guarda anche

* enum [ShadowType](../../shadowtype/)
* class [ShadowFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
