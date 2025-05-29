---
title: Document.RenderToScale
linktitle: RenderToScale
articleTitle: RenderToScale
second_title: Aspose.Words für .NET
description: Entdecken Sie die RenderToScale-Methode, um Dokumentseiten effizient in Grafikobjekte im gewünschten Maßstab zu rendern und so optimale visuelle Ergebnisse zu erzielen.
type: docs
weight: 730
url: /de/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

Rendert eine Dokumentseite in eineGraphics Objekt auf einen bestimmten Maßstab.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageIndex | Int32 | Der 0-basierte Seitenindex. |
| graphics | Graphics | Das Objekt, in das gerendert werden soll. |
| x | Single | Die X-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| y | Single | Die Y-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| scale | Single | Der Maßstab für die Darstellung der Seite (1,0 ist 100 %). |

### Rückgabewert

Die Breite und Höhe (in Welteinheiten) der gerenderten Seite.

## Beispiele

Zeigt, wie man aus den einzelnen Seiten eines Dokuments Grafiken macht, um ein Bild mit Miniaturansichten aller Seiten zu erstellen.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Berechnen Sie die Anzahl der Zeilen und Spalten, die wir mit Miniaturansichten füllen werden.
const int thumbColumns = 2;
int thumbRows = doc.PageCount / thumbColumns;
int remainder = doc.PageCount % thumbColumns;

if (remainder > 0)
    thumbRows++;

// Skalieren Sie die Miniaturansichten relativ zur Größe der ersten Seite.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Berechnen Sie die Größe des Bildes, das alle Miniaturansichten enthalten soll.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Füllen Sie den Hintergrund, der standardmäßig transparent ist, mit Weiß.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbColumns;
            int columnIdx = pageIndex % thumbColumns;

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

// Berechnen Sie die Anzahl der Zeilen und Spalten, die wir mit Miniaturansichten füllen werden.
const int thumbnailColumnsNum = 2;
int thumbRows = doc.PageCount / thumbnailColumnsNum;
int remainder = doc.PageCount % thumbnailColumnsNum;

if (remainder > 0)
    thumbRows++;

    // Skalieren Sie die Miniaturansichten relativ zur Größe der ersten Seite.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Berechnen Sie die Größe des Bildes, das alle Miniaturansichten enthalten soll.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Füllen Sie den Hintergrund, der standardmäßig transparent ist, mit Weiß.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbnailColumnsNum;
            int columnIdx = pageIndex % thumbnailColumnsNum;

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
