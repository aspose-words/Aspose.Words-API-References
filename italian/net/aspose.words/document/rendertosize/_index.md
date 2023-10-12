---
title: Document.RenderToSize
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Rende una pagina del documento in un fileGraphics oggetto a una dimensione specificata.
type: docs
weight: 710
url: /it/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Rende una pagina del documento in un fileGraphics oggetto a una dimensione specificata.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageIndex | Int32 | L'indice di pagina in base 0. |
| graphics | Graphics | L'oggetto su cui eseguire il rendering. |
| x | Single | La coordinata X (in unità mondiali) dell'angolo superiore sinistro della pagina renderizzata. |
| y | Single | La coordinata Y (in unità mondiali) dell'angolo superiore sinistro della pagina renderizzata. |
| width | Single | La larghezza massima (in unità mondiali) che può essere occupata dalla pagina sottoposta a rendering. |
| height | Single | L'altezza massima (in unità mondiali) che può essere occupata dalla pagina renderizzata. |

### Valore di ritorno

La scala calcolata automaticamente affinché la pagina sottoposta a rendering si adatti alla dimensione specificata.

### Esempi

Mostra come eseguire il rendering del documento come bitmap in una posizione e dimensione specificate (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Applica un fattore di scala del 70% alla pagina che renderemo utilizzando questa tela.
        canvas.Scale(70);

        // Sposta la pagina di 0,5" dai bordi superiore e sinistro della pagina.
        canvas.Translate(0.5f, 0.5f);

        // Ruota la pagina renderizzata di 10 gradi.
        canvas.RotateDegrees(10);

        // Crea e disegna un rettangolo.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Rende la prima pagina del documento alla stessa dimensione del rettangolo sopra.
        // Il rettangolo incornicerà questa pagina.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Reimposta la matrice, quindi applica una nuova serie di ridimensionamenti e traslazioni.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // Crea un altro rettangolo.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // Visualizza nuovamente la prima pagina all'interno del rettangolo appena creato.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Mostra come eseguire il rendering di un documento in una bitmap in una posizione e dimensione specificate.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Imposta la proprietà "PageUnit" su "GraphicsUnit.Inch" per utilizzare i pollici come file
        // unità di misura per eventuali trasformazioni e dimensioni che definiremo.
        gr.PageUnit = GraphicsUnit.Inch;

        // Sposta l'output a 0,5" dal bordo.
        gr.TranslateTransform(0.5f, 0.5f);

        // Ruota l'output di 10 gradi.
        gr.RotateTransform(10);

        // Disegna un rettangolo di 3"x3".
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Disegna la prima pagina del nostro documento con le stesse dimensioni e trasformazione del rettangolo.
        // Il rettangolo incornicerà la prima pagina.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Questo è il fattore di scala che il metodo RenderToSize ha applicato alla prima pagina per adattarla alla dimensione specificata.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Imposta la proprietà "PageUnit" su "GraphicsUnit.Millimeter" per utilizzare i millimetri come
        // unità di misura per eventuali trasformazioni e dimensioni che definiremo.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Reimposta le trasformazioni che abbiamo utilizzato dal rendering precedente.
        gr.ResetTransform();

        // Applica un'altra serie di trasformazioni.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Crea un altro rettangolo e usalo per incorniciare un'altra pagina del documento.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


