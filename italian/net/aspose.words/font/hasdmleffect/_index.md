---
title: Font.HasDmlEffect
linktitle: HasDmlEffect
articleTitle: HasDmlEffect
second_title: Aspose.Words per .NET
description: Scopri se uno specifico effetto di testo DrawingML è stato applicato con il metodo Font HasDmlEffect. Migliora l'aspetto visivo del tuo documento senza sforzo!
type: docs
weight: 570
url: /it/net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

Controlla se è stato applicato un particolare effetto di testo DrawingML.

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | Tipo di effetto testo DrawingML. |

### Valore di ritorno

`VERO` se viene applicato uno specifico effetto di testo DrawingML.

## Esempi

Mostra come verificare se un'esecuzione visualizza un effetto testo DrawingML.

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
