---
title: TextPath.SmallCaps
linktitle: SmallCaps
articleTitle: SmallCaps
second_title: Aspose.Words per .NET
description: Scopri la proprietà TextPath SmallCaps e formatta facilmente i caratteri in maiuscolo piccolo per una migliore leggibilità e un design del testo elegante.
type: docs
weight: 130
url: /it/net/aspose.words.drawing/textpath/smallcaps/
---
## TextPath.SmallCaps property

Vero se il font è formattato in maiuscolo minuscolo.

```csharp
public bool SmallCaps { get; set; }
```

## Osservazioni

Il valore predefinito è`falso`.

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

* class [TextPath](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
