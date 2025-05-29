---
title: TextEffect Enum
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words per .NET
description: Esplora l'enum Aspose.Words.TextEffect per animazioni di testo dinamiche. Arricchisci i tuoi documenti con effetti coinvolgenti per un'esperienza utente coinvolgente.
type: docs
weight: 7270
url: /it/net/aspose.words/texteffect/
---
## TextEffect enumeration

Effetto di animazione per le esecuzioni di testo.

```csharp
public enum TextEffect
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` |  |
| LasVegasLights | `1` |  |
| BlinkingBackground | `2` |  |
| SparkleText | `3` |  |
| MarchingBlackAnts | `4` |  |
| MarchingRedAnts | `5` |  |
| Shimmer | `6` |  |

## Esempi

Mostra come applicare un effetto visivo a una corsa.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Le versioni precedenti di Microsoft Word supportano solo gli effetti di animazione dei caratteri.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
