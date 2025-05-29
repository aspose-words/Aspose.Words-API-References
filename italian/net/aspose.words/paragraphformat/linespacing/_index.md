---
title: ParagraphFormat.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words per .NET
description: Regola facilmente l'interlinea dei tuoi paragrafi con la proprietà ParagraphFormat LineSpacing. Migliora la leggibilità e lo stile dei tuoi documenti!
type: docs
weight: 190
url: /it/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Ottiene o imposta la spaziatura delle linee (in punti) per il paragrafo.

```csharp
public double LineSpacing { get; set; }
```

## Osservazioni

Quando[`LineSpacingRule`](../linespacingrule/) la proprietà è impostata suAtLeast , la spaziatura delle linee può essere maggiore o uguale a, ma mai inferiore a quella specificata`LineSpacing` valore.

Quando[`LineSpacingRule`](../linespacingrule/) la proprietà è impostata suExactly , la spaziatura delle linee non cambia mai da quella specificata`LineSpacing` valore, anche se all'interno del paragrafo viene utilizzato un carattere più grande.

## Esempi

Mostra come lavorare con la spaziatura delle linee.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportate tre regole di spaziatura delle linee che possiamo definire utilizzando
// proprietà "LineSpacingRule" del paragrafo per configurare la spaziatura tra i paragrafi.
// 1 - Imposta una spaziatura minima.
// Questo darà una spaziatura verticale alle righe di testo di qualsiasi dimensione
// che è troppo piccolo per mantenere l'altezza minima della riga.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - Imposta la spaziatura esatta.
// L'utilizzo di dimensioni di carattere troppo grandi per la spaziatura troncherà il testo.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - Imposta la spaziatura come un multiplo dell'interlinea predefinita, che per impostazione predefinita è 12 punti.
// Questo tipo di spaziatura si adatta a diverse dimensioni del carattere.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
