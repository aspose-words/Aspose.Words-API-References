---
title: NumSpacing Enum
linktitle: NumSpacing
articleTitle: NumSpacing
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.NumSpacing per personalizzare la spaziatura dei numeri e migliorare la formattazione dei documenti. Migliora la presentazione del tuo testo oggi stesso!
type: docs
weight: 5030
url: /it/net/aspose.words/numspacing/
---
## NumSpacing enumeration

Specifica i possibili valori in cui può essere visualizzata la spaziatura numerica.

```csharp
public enum NumSpacing
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | `0` | Specifica che i numeri vengono visualizzati nel formato predefinito del font. |
| Proportional | `1` | Specifica che le forme dei numeri progettate come proporzionalmente distanziate vengono visualizzate se supportate dal font. |
| Tabular | `2` | Specifica che le forme dei numeri progettate come tabellari vengono visualizzate se supportate dal font. |

## Esempi

Mostra come impostare il tipo di spaziatura dei numeri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Questo effetto è supportato solo nelle versioni più recenti di MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
