---
title: Document.RenderToScale
linktitle: RenderToScale
articleTitle: RenderToScale
second_title: Aspose.Words für .NET
description: Document RenderToScale methode. Rendert eine Dokumentseite in eineGraphics Objekt in einem bestimmten Maßstab in C#.
type: docs
weight: 680
url: /de/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

Rendert eine Dokumentseite in eineGraphics Objekt in einem bestimmten Maßstab.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageIndex | Int32 | Der 0-basierte Seitenindex. |
| graphics | Graphics | Das Objekt, zu dem gerendert werden soll. |
| x | Single | Die X-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| y | Single | Die Y-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| scale | Single | Der Maßstab für die Darstellung der Seite (1,0 ist 100 %). |

### Rückgabewert

Die Breite und Höhe (in Welteinheiten) der gerenderten Seite.

## Beispiele

Zeigt, wie die einzelnen Seiten eines Dokuments in Grafiken umgewandelt werden, um ein Bild mit Miniaturansichten aller Seiten zu erstellen.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Berechnen Sie die Anzahl der Zeilen und Spalten, die wir mit Miniaturansichten füllen.
const int thumbColumns = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbColumns, out int remainder);

if (remainder > 0)
    thumbRows++;

// Skaliert die Miniaturansichten relativ zur Größe der ersten Seite.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Berechnen Sie die Größe des Bildes, das alle Miniaturansichten enthält.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Den Hintergrund, der standardmäßig transparent ist, mit Weiß füllen.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbColumns, out int columnIdx);

            // Geben Sie an, wo das Miniaturbild angezeigt werden soll.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // Rendern Sie eine Seite als Miniaturansicht und rahmen Sie sie dann in ein Rechteck derselben Größe ein.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

Rendert einzelne Seiten in Grafiken, um ein Bild mit Miniaturansichten aller Seiten zu erstellen (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Berechnen Sie die Anzahl der Zeilen und Spalten, die wir mit Miniaturansichten füllen.
const int thumbnailColumnsNum = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbnailColumnsNum, out int remainder);

if (remainder > 0)
    thumbRows++;

 // Skaliert die Miniaturansichten relativ zur Größe der ersten Seite.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Berechnen Sie die Größe des Bildes, das alle Miniaturansichten enthält.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Den Hintergrund, der standardmäßig transparent ist, mit Weiß füllen.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbnailColumnsNum, out int columnIdx);

            // Geben Sie an, wo das Miniaturbild angezeigt werden soll.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // Rendern Sie eine Seite als Miniaturansicht und rahmen Sie sie dann in ein Rechteck derselben Größe ein.
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

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
