---
title: LineSpacingRule Enum
linktitle: LineSpacingRule
articleTitle: LineSpacingRule
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.LineSpacingRule per personalizzare l'interlinea dei paragrafi. Migliora la formattazione dei documenti con un controllo preciso e una migliore leggibilità.
type: docs
weight: 3890
url: /it/net/aspose.words/linespacingrule/
---
## LineSpacingRule enumeration

Specifica i valori di spaziatura delle linee per un paragrafo.

```csharp
public enum LineSpacingRule
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| AtLeast | `0` | La spaziatura delle linee può essere maggiore o uguale, ma mai minore, del valore specificato nel[`LineSpacing`](../paragraphformat/linespacing/) proprietà. |
| Exactly | `1` | La spaziatura delle linee non cambia mai rispetto al valore specificato in [`LineSpacing`](../paragraphformat/linespacing/) proprietà, anche se all'interno del paragrafo viene utilizzato un font più grande. |
| Multiple | `2` | L'interlinea è specificata nel[`LineSpacing`](../paragraphformat/linespacing/) Proprietà come numero di linee. Una linea equivale a 12 punti. |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
