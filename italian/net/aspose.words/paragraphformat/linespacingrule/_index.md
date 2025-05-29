---
title: ParagraphFormat.LineSpacingRule
linktitle: LineSpacingRule
articleTitle: LineSpacingRule
second_title: Aspose.Words per .NET
description: Scopri la proprietà ParagraphFormat LineSpacingRule per personalizzare facilmente la spaziatura delle righe dei paragrafi, migliorando così la leggibilità e lo stile dei tuoi documenti.
type: docs
weight: 200
url: /it/net/aspose.words/paragraphformat/linespacingrule/
---
## ParagraphFormat.LineSpacingRule property

Ottiene o imposta la spaziatura delle righe per il paragrafo.

```csharp
public LineSpacingRule LineSpacingRule { get; set; }
```

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

* enum [LineSpacingRule](../../linespacingrule/)
* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
