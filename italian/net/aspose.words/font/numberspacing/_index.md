---
title: Font.NumberSpacing
linktitle: NumberSpacing
articleTitle: NumberSpacing
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font NumberSpacing per personalizzare la spaziatura dei numeri e migliorare la leggibilità e il design. Ottimizza la tua tipografia oggi stesso!
type: docs
weight: 290
url: /it/net/aspose.words/font/numberspacing/
---
## Font.NumberSpacing property

Ottiene o imposta il tipo di spaziatura del numero visualizzato.

```csharp
public NumSpacing NumberSpacing { get; set; }
```

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

* enum [NumSpacing](../../numspacing/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
