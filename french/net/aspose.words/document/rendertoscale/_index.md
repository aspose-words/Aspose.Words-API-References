---
title: RenderToScale
second_title: Référence de l'API Aspose.Words pour .NET
description: Rend une page de document dans unGraphics objet à une échelle spécifiée.
type: docs
weight: 660
url: /fr/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

Rend une page de document dans unGraphics objet à une échelle spécifiée.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pageIndex | Int32 | L'index de page basé sur 0. |
| graphics | Graphics | L'objet vers lequel effectuer le rendu. |
| x | Single | La coordonnée X (en unités universelles) du coin supérieur gauche de la page rendue. |
| y | Single | La coordonnée Y (en unités universelles) du coin supérieur gauche de la page rendue. |
| scale | Single | L'échelle de rendu de la page (1.0 correspond à 100 %). |

### Return_Value

La largeur et la hauteur (en unités universelles) de la page rendue.

### Exemples

Montre comment les pages individuelles d'un document aux graphiques pour créer une image avec des vignettes de toutes les pages.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Calcule le nombre de lignes et de colonnes que nous remplirons de vignettes.
const int thumbColumns = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbColumns, out int remainder);

if (remainder > 0)
    thumbRows++;

// Redimensionne les vignettes par rapport à la taille de la première page.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Calcule la taille de l'image qui contiendra toutes les vignettes.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Remplit le fond, qui est transparent par défaut, en blanc.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbColumns, out int columnIdx);

            // Spécifiez où nous voulons que la vignette apparaisse.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // Afficher une page sous forme de vignette, puis l'encadrer dans un rectangle de même taille.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

Rend les pages individuelles en graphiques pour créer une image avec des vignettes de toutes les pages (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Calcule le nombre de lignes et de colonnes que nous remplirons de vignettes.
const int thumbnailColumnsNum = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbnailColumnsNum, out int remainder);

if (remainder > 0)
    thumbRows++;

 // Redimensionne les vignettes par rapport à la taille de la première page.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Calcule la taille de l'image qui contiendra toutes les vignettes.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Remplit le fond, qui est transparent par défaut, en blanc.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbnailColumnsNum, out int columnIdx);

            // Spécifiez où nous voulons que la vignette apparaisse.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // Afficher une page sous forme de vignette, puis l'encadrer dans un rectangle de même taille.
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

### Voir également

* class [Document](../../document)
* espace de noms [Aspose.Words](../../document)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
