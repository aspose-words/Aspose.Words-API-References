---
title: Document.RenderToSize
linktitle: RenderToSize
articleTitle: RenderToSize
second_title: Aspose.Words pour .NET
description: Découvrez la méthode RenderToSize pour convertir efficacement des pages de documents en objets graphiques aux dimensions souhaitées. Améliorez votre rendu dès aujourd'hui !
type: docs
weight: 740
url: /fr/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Rend une page de document dans unGraphics objet à une taille spécifiée.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pageIndex | Int32 | L'index de page basé sur 0. |
| graphics | Graphics | L'objet vers lequel effectuer le rendu. |
| x | Single | La coordonnée X (en unités mondiales) du coin supérieur gauche de la page rendue. |
| y | Single | La coordonnée Y (en unités mondiales) du coin supérieur gauche de la page rendue. |
| width | Single | La largeur maximale (en unités mondiales) qui peut être occupée par la page rendue. |
| height | Single | La hauteur maximale (en unités mondiales) qui peut être occupée par la page rendue. |

### Return_Value

L'échelle qui a été automatiquement calculée pour que la page rendue s'adapte à la taille spécifiée.

## Exemples

Montre comment restituer le document sous forme de bitmap à un emplacement et à une taille spécifiés (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Appliquez un facteur d'échelle de 70 % à la page que nous allons rendre à l'aide de ce canevas.
        canvas.Scale(70);

        // Décalez la page de 0,5" à partir des bords supérieur et gauche de la page.
        canvas.Translate(0.5f, 0.5f);

        // Faites pivoter la page rendue de 10 degrés.
        canvas.RotateDegrees(10);

        // Créez et dessinez un rectangle.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Rendre la première page du document à la même taille que le rectangle ci-dessus.
        // Le rectangle encadrera cette page.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Réinitialisez la matrice, puis appliquez un nouvel ensemble de mises à l'échelle et de traductions.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // Créez un autre rectangle.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // Rendre à nouveau la première page dans le rectangle nouvellement créé.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Montre comment restituer un document en bitmap à un emplacement et à une taille spécifiés.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Définissez la propriété « PageUnit » sur « GraphicsUnit.Inch » pour utiliser les pouces comme
        // unité de mesure pour toutes les transformations et dimensions que nous définirons.
        gr.PageUnit = GraphicsUnit.Inch;

        // Décalez la sortie de 0,5" par rapport au bord.
        gr.TranslateTransform(0.5f, 0.5f);

        // Faites pivoter la sortie de 10 degrés.
        gr.RotateTransform(10);

        // Dessinez un rectangle de 3"x3".
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Dessinez la première page de notre document avec les mêmes dimensions et transformation que le rectangle.
        // Le rectangle encadrera la première page.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Il s'agit du facteur d'échelle que la méthode RenderToSize a appliqué à la première page pour s'adapter à la taille spécifiée.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Définissez la propriété « PageUnit » sur « GraphicsUnit.Millimeter » pour utiliser les millimètres comme
        // unité de mesure pour toutes les transformations et dimensions que nous définirons.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Réinitialiser les transformations que nous avons utilisées à partir du rendu précédent.
        gr.ResetTransform();

         // Appliquer un autre ensemble de transformations.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Créez un autre rectangle et utilisez-le pour encadrer une autre page du document.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
