---
title: ShadowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShadowFormat Color per personalizzare i colori delle ombre nei tuoi progetti. Il colore predefinito è il nero, ma libera la tua creatività con opzioni vivaci!
type: docs
weight: 10
url: /it/net/aspose.words.drawing/shadowformat/color/
---
## ShadowFormat.Color property

Ottiene unColor oggetto che rappresenta il colore dell'ombra. Il valore predefinito èBlack .

```csharp
public Color Color { get; }
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

* class [ShadowFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
