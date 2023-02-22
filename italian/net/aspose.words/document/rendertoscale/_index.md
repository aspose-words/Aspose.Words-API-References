---
title: Document.RenderToScale
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Rendering di una pagina del documento in aGraphics oggetto su una scala specificata.
type: docs
weight: 660
url: /it/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

Rendering di una pagina del documento in aGraphics oggetto su una scala specificata.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageIndex | Int32 | L'indice della pagina in base 0. |
| graphics | Graphics | L'oggetto su cui eseguire il rendering. |
| x | Single | La coordinata X (in unità mondiali) dell'angolo in alto a sinistra della pagina sottoposta a rendering. |
| y | Single | La coordinata Y (in unità mondiali) dell'angolo superiore sinistro della pagina sottoposta a rendering. |
| scale | Single | La scala per il rendering della pagina (1,0 è 100%). |

### Valore di ritorno

La larghezza e l'altezza (in unità mondiali) della pagina sottoposta a rendering.

### Esempi

Mostra come le singole pagine di un documento alla grafica per creare un'immagine con le miniature di tutte le pagine.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Calcola il numero di righe e colonne che andremo a riempire con le miniature.
const int thumbColumns = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbColumns, out int remainder);

if (remainder > 0)
    thumbRows++;

// Ridimensiona le miniature rispetto alle dimensioni della prima pagina.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Calcola la dimensione dell'immagine che conterrà tutte le miniature.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Riempi lo sfondo, che è trasparente per impostazione predefinita, in bianco.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbColumns, out int columnIdx);

            // Specifica dove vogliamo che appaia la miniatura.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // Visualizza una pagina come miniatura, quindi inquadrala in un rettangolo della stessa dimensione.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

Rendering di singole pagine in grafica per creare un'immagine con le miniature di tutte le pagine (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Calcola il numero di righe e colonne che andremo a riempire con le miniature.
const int thumbnailColumnsNum = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbnailColumnsNum, out int remainder);

if (remainder > 0)
    thumbRows++;

 // Ridimensiona le miniature rispetto alle dimensioni della prima pagina.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Calcola la dimensione dell'immagine che conterrà tutte le miniature.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Riempi lo sfondo, che è trasparente per impostazione predefinita, in bianco.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbnailColumnsNum, out int columnIdx);

            // Specifica dove vogliamo che appaia la miniatura.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // Visualizza una pagina come miniatura, quindi inquadrala in un rettangolo della stessa dimensione.
            SKRect rect = new SKRect(0, 0, size.Width, size.Height);
            rect.Offset(thumbLeft, thumbTop);
            canvas.DrawRect(rect, new SKPaint
            {
                Color = SKColors.Black,
                Style = SKPaintStyle.Stroke
            });
        }

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.CreateThumbnailsNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


