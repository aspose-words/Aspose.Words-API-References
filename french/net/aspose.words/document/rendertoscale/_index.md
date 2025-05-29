---
title: Document.RenderToScale
linktitle: RenderToScale
articleTitle: RenderToScale
second_title: Aspose.Words pour .NET
description: Découvrez la méthode RenderToScale pour restituer efficacement les pages de documents en objets graphiques à l'échelle souhaitée pour des résultats visuels optimaux.
type: docs
weight: 730
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
| x | Single | La coordonnée X (en unités mondiales) du coin supérieur gauche de la page rendue. |
| y | Single | La coordonnée Y (en unités mondiales) du coin supérieur gauche de la page rendue. |
| scale | Single | L'échelle de rendu de la page (1,0 est 100%). |

### Return_Value

La largeur et la hauteur (en unités mondiales) de la page rendue.

## Exemples

Montre comment convertir les pages individuelles d'un document en graphiques pour créer une image avec des miniatures de toutes les pages.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Calculez le nombre de lignes et de colonnes que nous allons remplir avec des vignettes.
const int thumbColumns = 2;
int thumbRows = doc.PageCount / thumbColumns;
int remainder = doc.PageCount % thumbColumns;

if (remainder > 0)
    thumbRows++;

// Mettez les vignettes à l'échelle par rapport à la taille de la première page.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Calculez la taille de l'image qui contiendra toutes les vignettes.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Remplissez l'arrière-plan, qui est transparent par défaut, en blanc.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbColumns;
            int columnIdx = pageIndex % thumbColumns;

            // Spécifiez où nous voulons que la vignette apparaisse.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // Affichez une page sous forme de vignette, puis encadrez-la dans un rectangle de la même taille.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

Convertit des pages individuelles en graphiques pour créer une image avec des miniatures de toutes les pages (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Calculez le nombre de lignes et de colonnes que nous allons remplir avec des vignettes.
const int thumbnailColumnsNum = 2;
int thumbRows = doc.PageCount / thumbnailColumnsNum;
int remainder = doc.PageCount % thumbnailColumnsNum;

if (remainder > 0)
    thumbRows++;

 // Mettez les vignettes à l'échelle par rapport à la taille de la première page.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Calculez la taille de l'image qui contiendra toutes les vignettes.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Remplissez l'arrière-plan, qui est transparent par défaut, en blanc.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbnailColumnsNum;
            int columnIdx = pageIndex % thumbnailColumnsNum;

            // Spécifiez où nous voulons que la vignette apparaisse.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // Affichez une page sous forme de vignette, puis encadrez-la dans un rectangle de la même taille.
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

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
