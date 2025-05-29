---
title: Document.RenderToScale
linktitle: RenderToScale
articleTitle: RenderToScale
second_title: Aspose.Words för .NET
description: Upptäck RenderToScale-metoden för att effektivt rendera dokumentsidor till grafikobjekt i önskad skala för optimala visuella resultat.
type: docs
weight: 730
url: /sv/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

Återger en dokumentsida till enGraphics objekt i en specificerad skala.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pageIndex | Int32 | Det 0-baserade sidindexet. |
| graphics | Graphics | Objektet dit det ska renderas. |
| x | Single | X-koordinaten (i världsenheter) för det övre vänstra hörnet av den renderade sidan. |
| y | Single | Y-koordinaten (i världsenheter) för det övre vänstra hörnet av den renderade sidan. |
| scale | Single | Skalan för att rendera sidan (1.0 är 100%). |

### Returvärde

Bredden och höjden (i världsenheter) på den renderade sidan.

## Exempel

Visar hur man omvandlar de enskilda sidorna i ett dokument till grafik för att skapa en bild med miniatyrbilder av alla sidor.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Beräkna antalet rader och kolumner som vi ska fylla med miniatyrbilder.
const int thumbColumns = 2;
int thumbRows = doc.PageCount / thumbColumns;
int remainder = doc.PageCount % thumbColumns;

if (remainder > 0)
    thumbRows++;

// Skala miniatyrbilderna i förhållande till storleken på den första sidan.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Beräkna storleken på bilden som ska innehålla alla miniatyrbilder.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Fyll bakgrunden, som är transparent som standard, med vitt.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbColumns;
            int columnIdx = pageIndex % thumbColumns;

            // Ange var vi vill att miniatyrbilden ska visas.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // Rendera en sida som en miniatyrbild och rama sedan in den i en rektangel av samma storlek.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

Renderar enskilda sidor till grafik för att skapa en bild med miniatyrbilder av alla sidor (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Beräkna antalet rader och kolumner som vi ska fylla med miniatyrbilder.
const int thumbnailColumnsNum = 2;
int thumbRows = doc.PageCount / thumbnailColumnsNum;
int remainder = doc.PageCount % thumbnailColumnsNum;

if (remainder > 0)
    thumbRows++;

 // Skala miniatyrbilderna i förhållande till storleken på den första sidan.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Beräkna storleken på bilden som ska innehålla alla miniatyrbilder.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Fyll bakgrunden, som är transparent som standard, med vitt.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbnailColumnsNum;
            int columnIdx = pageIndex % thumbnailColumnsNum;

            // Ange var vi vill att miniatyrbilden ska visas.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // Rendera en sida som en miniatyrbild och rama sedan in den i en rektangel av samma storlek.
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

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
