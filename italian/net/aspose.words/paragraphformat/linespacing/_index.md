---
title: ParagraphFormat.LineSpacing
second_title: Aspose.Words per .NET API Reference
description: ParagraphFormat proprietà. Ottiene o imposta linterlinea in punti per il paragrafo.
type: docs
weight: 190
url: /it/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Ottiene o imposta l'interlinea (in punti) per il paragrafo.

```csharp
public double LineSpacing { get; set; }
```

### Osservazioni

Quando[`LineSpacingRule`](../linespacingrule/) la proprietà è impostata suAtLeast , l'interlinea può essere maggiore o uguale a, ma mai inferiore a quella specificata`LineSpacing` valore.

Quando[`LineSpacingRule`](../linespacingrule/) la proprietà è impostata suExactly , l'interlinea non cambia mai da a quella specificata`LineSpacing` valore, anche se all'interno del paragrafo viene utilizzato un carattere più grande.

### Esempi

Mostra come lavorare con l'interlinea.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportate tre regole di interlinea che possiamo definire utilizzando il file
// la proprietà "LineSpacingRule" del paragrafo per configurare la spaziatura tra i paragrafi.
// 1 - Imposta una quantità minima di spaziatura.
// Ciò darà un riempimento verticale alle righe di testo di qualsiasi dimensione
// è troppo piccolo per mantenere l'altezza minima della riga.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - Imposta la spaziatura esatta.
// L'utilizzo di dimensioni dei caratteri troppo grandi per la spaziatura troncherà il testo.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - Imposta la spaziatura come multiplo dell'interlinea predefinita, che per impostazione predefinita è 12 punti.
// Questo tipo di spaziatura verrà adattato alle diverse dimensioni dei caratteri.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../paragraphformat/)
* assemblea [Aspose.Words](../../../)


