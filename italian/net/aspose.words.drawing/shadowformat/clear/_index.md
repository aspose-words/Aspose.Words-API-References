---
title: ShadowFormat.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words per .NET
description: Ripristina senza sforzo il formato delle tue ombre con il metodo ShadowFormat Clear. Migliora il tuo design con una tabula rasa oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Cancella il formato ombra.

```csharp
public void Clear()
```

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
