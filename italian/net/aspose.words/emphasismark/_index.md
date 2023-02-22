---
title: Enum EmphasisMark
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.EmphasisMark enum. Specifica i possibili tipi di segno di enfasi.
type: docs
weight: 1310
url: /it/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Specifica i possibili tipi di segno di enfasi.

```csharp
public enum EmphasisMark
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Nessun segno di enfasi. |
| OverSolidCircle | `1` | Il segno di enfasi è un cerchio nero pieno visualizzato sopra il testo. |
| OverComma | `2` | Il segno di enfasi è un carattere virgola visualizzato sopra il testo. |
| OverWhiteCircle | `3` | Il segno di enfasi è un cerchio bianco vuoto visualizzato sopra il testo. |
| UnderSolidCircle | `4` | Il segno di enfasi è un cerchio nero pieno visualizzato sotto il testo. |

### Esempi

Mostra come aggiungere un carattere aggiuntivo visualizzato sopra/sotto il carattere glifo.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Possibili tipi di enfasi:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


