---
title: Font.HasDmlEffect
linktitle: HasDmlEffect
articleTitle: HasDmlEffect
second_title: Aspose.Words per .NET
description: Font HasDmlEffect metodo. Controlla se viene applicato un particolare effetto di testo DrawingML in C#.
type: docs
weight: 560
url: /it/net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

Controlla se viene applicato un particolare effetto di testo DrawingML.

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | Tipo di effetto testo DrawingML. |

### Valore di ritorno

`VERO` se viene applicato un particolare effetto di testo DrawingML.

## Esempi

Mostra come verificare se un'esecuzione visualizza un effetto di testo DrawingML.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### Guarda anche

* enum [TextDmlEffect](../../textdmleffect/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
