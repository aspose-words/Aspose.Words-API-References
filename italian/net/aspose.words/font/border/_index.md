---
title: Font.Border
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Restituisce aBorder oggetto che specifica il bordo per il font.
type: docs
weight: 60
url: /it/net/aspose.words/font/border/
---
## Font.Border property

Restituisce a[`Border`](../../border/) oggetto che specifica il bordo per il font.

```csharp
public Border Border { get; }
```

### Esempi

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
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


