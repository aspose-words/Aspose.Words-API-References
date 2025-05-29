---
title: Document.RenderToSize
linktitle: RenderToSize
articleTitle: RenderToSize
second_title: Aspose.Words per .NET
description: Scopri il metodo RenderToSize per convertire in modo efficiente le pagine dei documenti in oggetti grafici delle dimensioni desiderate. Migliora il tuo processo di rendering oggi stesso!
type: docs
weight: 740
url: /it/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Rende una pagina del documento in unGraphics oggetto a una dimensione specificata.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageIndex | Int32 | Indice di pagina basato su 0. |
| graphics | Graphics | L'oggetto su cui effettuare il rendering. |
| x | Single | Coordinata X (in unità mondiali) dell'angolo in alto a sinistra della pagina visualizzata. |
| y | Single | Coordinata Y (in unità mondiali) dell'angolo in alto a sinistra della pagina visualizzata. |
| width | Single | Larghezza massima (in unità mondiali) che può essere occupata dalla pagina renderizzata. |
| height | Single | L'altezza massima (in unità mondiali) che può essere occupata dalla pagina renderizzata. |

### Valore di ritorno

La scala calcolata automaticamente per adattare la pagina renderizzata alle dimensioni specificate.

## Esempi

Mostra come rendere il documento come bitmap in una posizione e dimensione specificate (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Applichiamo un fattore di scala del 70% alla pagina che verrà renderizzata utilizzando questa tela.
        canvas.Scale(70);

        // Spostare la pagina di 0,5" dai bordi superiore e sinistro della pagina.
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

        // Rendi la prima pagina del documento della stessa dimensione del rettangolo soprastante.
        // Il rettangolo incornicerà questa pagina.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Reimposta la matrice, quindi applica un nuovo set di ridimensionamento e traslazioni.
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

        // Esegui nuovamente il rendering della prima pagina all'interno del rettangolo appena creato.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Mostra come trasformare un documento in un'immagine bitmap in una posizione e con dimensioni specifiche.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Imposta la proprietà "PageUnit" su "GraphicsUnit.Inch" per utilizzare i pollici come
        // unità di misura per tutte le trasformazioni e le dimensioni che definiremo.
        gr.PageUnit = GraphicsUnit.Inch;

        // Sposta l'output di 0,5" dal bordo.
        gr.TranslateTransform(0.5f, 0.5f);

        // Ruota l'output di 10 gradi.
        gr.RotateTransform(10);

        // Disegna un rettangolo di 3"x3".
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Disegna la prima pagina del nostro documento con le stesse dimensioni e trasformazione del rettangolo.
        // Il rettangolo incornicerà la prima pagina.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Questo è il fattore di scala applicato dal metodo RenderToSize alla prima pagina per adattarla alle dimensioni specificate.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Imposta la proprietà "PageUnit" su "GraphicsUnit.Millimeter" per utilizzare i millimetri come
        // unità di misura per tutte le trasformazioni e le dimensioni che definiremo.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Reimposta le trasformazioni utilizzate nel rendering precedente.
        gr.ResetTransform();

         // Applica un altro set di trasformazioni.
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
