---
title: ParagraphFormat.Borders
second_title: Aspose.Words per .NET API Reference
description: ParagraphFormat proprietà. Ottiene la raccolta dei bordi del paragrafo.
type: docs
weight: 50
url: /it/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

Ottiene la raccolta dei bordi del paragrafo.

```csharp
public BorderCollection Borders { get; }
```

### Esempi

Mostra come inserire un paragrafo con un bordo superiore.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Guarda anche

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../paragraphformat/)
* assemblea [Aspose.Words](../../../)


