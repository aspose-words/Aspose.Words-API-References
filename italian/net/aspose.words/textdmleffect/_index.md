---
title: TextDmlEffect Enum
linktitle: TextDmlEffect
articleTitle: TextDmlEffect
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.TextDmlEffect per migliorare le sequenze di testo con effetti DML dinamici. Migliora la presentazione dei tuoi documenti senza sforzo!
type: docs
weight: 7260
url: /it/net/aspose.words/textdmleffect/
---
## TextDmlEffect enumeration

Effetto testo Dml per sequenze di testo.

```csharp
public enum TextDmlEffect
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Glow | `0` | Effetto bagliore, in cui un contorno sfocato colorato viene aggiunto all'esterno dei bordi dell'oggetto. |
| Fill | `1` | Effetto sovrapposizione riempimento. |
| Shadow | `2` | Effetto ombra. |
| Outline | `3` | Effetto contorno. |
| Effect3D | `4` | Effetto 3D. |
| Reflection | `5` | Effetto riflesso. |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
