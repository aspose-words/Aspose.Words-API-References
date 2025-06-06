---
title: TextPath Class
linktitle: TextPath
articleTitle: TextPath
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.TextPath per creare splendide WordArt. Definisci facilmente testo e formattazione per migliorare i tuoi documenti.
type: docs
weight: 1760
url: /it/net/aspose.words.drawing/textpath/
---
## TextPath class

Definisce il testo e la formattazione del percorso di testo (di un oggetto WordArt).

Per saperne di più, visita il[Lavorare con le forme](https://docs.aspose.com/words/net/working-with-shapes/) articolo di documentazione.

```csharp
public class TextPath
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bold](../../aspose.words.drawing/textpath/bold/) { get; set; } | Vero se il font è formattato in grassetto. |
| [FitPath](../../aspose.words.drawing/textpath/fitpath/) { get; set; } | Definisce se il testo si adatta al percorso di una forma. |
| [FitShape](../../aspose.words.drawing/textpath/fitshape/) { get; set; } | Definisce se il testo si adatta al riquadro di delimitazione di una forma. |
| [FontFamily](../../aspose.words.drawing/textpath/fontfamily/) { get; set; } | Definisce la famiglia del font del percorso di testo. |
| [Italic](../../aspose.words.drawing/textpath/italic/) { get; set; } | Vero se il font è formattato in corsivo. |
| [Kerning](../../aspose.words.drawing/textpath/kerning/) { get; set; } | Determina se la crenatura è attivata. |
| [On](../../aspose.words.drawing/textpath/on/) { get; set; } | Definisce se il testo viene visualizzato. |
| [ReverseRows](../../aspose.words.drawing/textpath/reverserows/) { get; set; } | Determina se l'ordine di disposizione delle righe è invertito. |
| [RotateLetters](../../aspose.words.drawing/textpath/rotateletters/) { get; set; } | Determina se le lettere del testo vengono ruotate. |
| [SameLetterHeights](../../aspose.words.drawing/textpath/sameletterheights/) { get; set; } | Determina se tutte le lettere avranno la stessa altezza indipendentemente dalla lettera iniziale. |
| [Shadow](../../aspose.words.drawing/textpath/shadow/) { get; set; } | Definisce se un'ombra viene applicata al testo su un percorso di testo. |
| [Size](../../aspose.words.drawing/textpath/size/) { get; set; } | Definisce la dimensione del carattere in punti. |
| [SmallCaps](../../aspose.words.drawing/textpath/smallcaps/) { get; set; } | Vero se il font è formattato in maiuscolo minuscolo. |
| [Spacing](../../aspose.words.drawing/textpath/spacing/) { get; set; } | Definisce la quantità di spaziatura per il testo. 1 significa 100%. |
| [StrikeThrough](../../aspose.words.drawing/textpath/strikethrough/) { get; set; } | Vero se il font è formattato come testo barrato. |
| [Text](../../aspose.words.drawing/textpath/text/) { get; set; } | Definisce il testo del percorso di testo. |
| [TextPathAlignment](../../aspose.words.drawing/textpath/textpathalignment/) { get; set; } | Definisce l'allineamento del testo. |
| [Trim](../../aspose.words.drawing/textpath/trim/) { get; set; } | Determina se lo spazio extra viene rimosso sopra e sotto il testo. |
| [Underline](../../aspose.words.drawing/textpath/underline/) { get; set; } | Vero se il carattere è sottolineato. |
| [XScale](../../aspose.words.drawing/textpath/xscale/) { get; set; } | Determina se verrà utilizzato un percorso di testo dritto al posto del percorso di forma. |

## Osservazioni

Utilizzare il[`TextPath`](../shape/textpath/) proprietà per accedere alle proprietà WordArt di una forma. Non creare istanze di`TextPath` classe direttamente.

## Esempi

Mostra come lavorare con WordArt.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // Inserire un oggetto WordArt per visualizzare il testo in una forma che possiamo ridimensionare e spostare utilizzando il mouse in Microsoft Word.
    // Fornire "ShapeType" come argomento per impostare una forma per WordArt.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.",
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Applica le impostazioni di formattazione "Grassetto" e "Corsivo" al testo utilizzando le rispettive proprietà.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // Di seguito sono riportate altre proprietà relative alla formattazione del testo.
    Assert.False(shape.TextPath.Underline);
    Assert.False(shape.TextPath.Shadow);
    Assert.False(shape.TextPath.StrikeThrough);
    Assert.False(shape.TextPath.ReverseRows);
    Assert.False(shape.TextPath.XScale);
    Assert.False(shape.TextPath.Trim);
    Assert.False(shape.TextPath.SmallCaps);

    Assert.AreEqual(36.0, shape.TextPath.Size);
    Assert.AreEqual("Hello World! This text is bold, and italic.", shape.TextPath.Text);
    Assert.AreEqual(ShapeType.TextPlainText, shape.ShapeType);

    // Utilizzare la proprietà "On" per mostrare/nascondere il testo.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Utilizzare la proprietà "Kerning" per abilitare/disabilitare la spaziatura del kerning tra determinati caratteri.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Utilizzare la proprietà "Spaziatura" per impostare la spaziatura personalizzata tra i caratteri su una scala da 0,0 (nessuna) a 1,0 (predefinita).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Imposta la proprietà "RotateLetters" su "true" per ruotare ogni carattere di 90 gradi in senso antiorario.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Impostare la proprietà "SameLetterHeights" su "true" per far sì che l'altezza x di ciascun carattere sia uguale all'altezza della maiuscola.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // Per impostazione predefinita, la dimensione del testo verrà sempre ridimensionata per adattarsi alla dimensione della forma che la contiene, ignorando l'impostazione della dimensione del testo.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Se impostiamo la proprietà "FitShape:" su "false", il testo manterrà la dimensione
    // che la proprietà "Size" specifica indipendentemente dalla dimensione della forma.
    // Utilizzare la proprietà "TextPathAlignment" anche per allineare il testo a un lato della forma.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// Inserisci un nuovo paragrafo con una forma WordArt al suo interno.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Crea una forma in linea, che servirà da contenitore per il nostro WordArt.
    // La forma può essere una forma WordArt valida solo se le assegniamo uno ShapeType designato da WordArt.
    // Questi tipi avranno "oggetto WordArt" nella descrizione,
    // e i nomi delle loro costanti enumeratrici inizieranno tutti con "Text".
    Shape shape = new Shape(doc, wordArtShapeType)
    {
        WrapType = WrapType.Inline,
        Width = shapeWidth,
        Height = shapeHeight,
        FillColor = wordArtFill,
        StrokeColor = line
    };

    shape.TextPath.Text = text;
    shape.TextPath.FontFamily = textFontFamily;

    Paragraph para = (Paragraph)doc.FirstSection.Body.AppendChild(new Paragraph(doc));
    para.AppendChild(shape);
    return shape;
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
