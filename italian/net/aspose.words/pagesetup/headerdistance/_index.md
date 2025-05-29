---
title: PageSetup.HeaderDistance
linktitle: HeaderDistance
articleTitle: HeaderDistance
second_title: Aspose.Words per .NET
description: Regola la proprietà HeaderDistance di PageSetup per personalizzare la spaziatura delle intestazioni in punti, migliorando il layout del documento per una migliore leggibilità e presentazione.
type: docs
weight: 170
url: /it/net/aspose.words/pagesetup/headerdistance/
---
## PageSetup.HeaderDistance property

Restituisce o imposta la distanza (in punti) tra l'intestazione e la parte superiore della pagina.

```csharp
public double HeaderDistance { get; set; }
```

## Esempi

Mostra come regolare il formato della carta, l'orientamento, i margini e altre impostazioni per una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
