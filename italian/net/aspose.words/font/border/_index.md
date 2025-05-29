---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font Border, che fornisce un oggetto Border personalizzabile per migliorare lo stile del tuo font e la flessibilità del design.
type: docs
weight: 60
url: /it/net/aspose.words/font/border/
---
## Font.Border property

Restituisce un[`Border`](../../border/) oggetto che specifica il bordo per il font.

```csharp
public Border Border { get; }
```

## Esempi

Mostra come inserire una stringa circondata da un bordo in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Guarda anche

* class [Border](../../border/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
