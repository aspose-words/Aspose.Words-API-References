---
title: TextBox Class
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.TextBox per personalizzare facilmente la visualizzazione del testo all'interno delle forme, migliorando l'aspetto visivo e la funzionalità del tuo documento.
type: docs
weight: 1730
url: /it/net/aspose.words.drawing/textbox/
---
## TextBox class

Definisce gli attributi che specificano come viene visualizzato un testo all'interno di una forma.

Per saperne di più, visita il[Lavorare con le forme](https://docs.aspose.com/words/net/working-with-shapes/) articolo di documentazione.

```csharp
public class TextBox
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | Determina se Microsoft Word ingrandirà la forma per adattarla al testo. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | Specifica il margine inferiore interno in punti per una forma. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | Specifica il margine interno sinistro in punti per una forma. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | Specifica il margine interno destro in punti per una forma. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | Specifica il margine superiore interno in punti per una forma. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | Determina il flusso del layout del testo in una forma. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | Restituisce o imposta un`TextBox` che rappresenta il prossimo`TextBox`in una sequenza di forme. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | Ottiene o imposta un valore booleano che indica che il testo della TextBox non deve ruotare quando la forma viene ruotata. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | Ottiene una forma padre per il`TextBox` . |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | Restituisce un`TextBox` che rappresenta il precedente`TextBox`in una sequenza di forme. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | Determina come il testo viene disposto all'interno di una forma. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | Specifica l'allineamento verticale del testo all'interno di una forma. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | Interrompe il collegamento al successivo`TextBox` . |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | Determina se questo`TextBox` può essere collegato al target`TextBox` . |

## Osservazioni

Utilizzare il[`TextBox`](../shape/textbox/) proprietà per accedere alle proprietà del testo di una forma. Non si creano istanze di`TextBox` classe direttamente.

## Esempi

Mostra come impostare i margini interni per una casella di testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un'altra casella di testo con margini specifici.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

Mostra come impostare l'orientamento del testo all'interno di una casella di testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Sposta il generatore di documenti all'interno della TextBox e aggiungi il testo.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Imposta la proprietà "LayoutFlow" per impostare un orientamento per il contenuto di testo di questa casella di testo.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

Mostra come ridimensionare una casella di testo per adattarla perfettamente al suo contenuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Applica questi valori a entrambi i membri per adattare la forma padre
// strettamente attorno al contenuto del testo, ignorando le dimensioni che abbiamo impostato.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
