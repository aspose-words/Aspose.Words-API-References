---
title: Document.RenderToScale
linktitle: RenderToScale
articleTitle: RenderToScale
second_title: Aspose.Words per .NET
description: Scopri il metodo RenderToScale per trasformare in modo efficiente le pagine dei documenti in oggetti grafici nella scala desiderata, ottenendo risultati visivi ottimali.
type: docs
weight: 730
url: /it/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

Rende una pagina del documento in unGraphics oggetto a una scala specificata.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageIndex | Int32 | Indice di pagina basato su 0. |
| graphics | Graphics | L'oggetto su cui effettuare il rendering. |
| x | Single | Coordinata X (in unità mondiali) dell'angolo in alto a sinistra della pagina visualizzata. |
| y | Single | Coordinata Y (in unità mondiali) dell'angolo in alto a sinistra della pagina visualizzata. |
| scale | Single | Scala per il rendering della pagina (1.0 è 100%). |

### Valore di ritorno

Larghezza e altezza (in unità mondiali) della pagina renderizzata.

## Esempi

Mostra come trasformare le singole pagine di un documento in grafici per creare un'immagine con le miniature di tutte le pagine.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Calcola il numero di righe e colonne che riempiremo con le miniature.
const int thumbColumns = 2;
int thumbRows = doc.PageCount / thumbColumns;
int remainder = doc.PageCount % thumbColumns;

if (remainder > 0)
    thumbRows++;

// Adatta le miniature alle dimensioni della prima pagina.
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

        // Riempi lo sfondo, che per impostazione predefinita è trasparente, di bianco.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbColumns;
            int columnIdx = pageIndex % thumbColumns;

            // Specifica dove vogliamo che appaia la miniatura.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // Rendi una pagina come miniatura, quindi incorniciala in un rettangolo delle stesse dimensioni.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

Esegue il rendering delle singole pagine in grafica per creare un'immagine con le miniature di tutte le pagine (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Calcola il numero di righe e colonne che riempiremo con le miniature.
const int thumbnailColumnsNum = 2;
int thumbRows = doc.PageCount / thumbnailColumnsNum;
int remainder = doc.PageCount % thumbnailColumnsNum;

if (remainder > 0)
    thumbRows++;

 // Adatta le miniature alle dimensioni della prima pagina.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Calcola la dimensione dell'immagine che conterrà tutte le miniature.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Riempi lo sfondo, che per impostazione predefinita è trasparente, di bianco.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbnailColumnsNum;
            int columnIdx = pageIndex % thumbnailColumnsNum;

            // Specifica dove vogliamo che appaia la miniatura.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // Rendi una pagina come miniatura, quindi incorniciala in un rettangolo delle stesse dimensioni.
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
