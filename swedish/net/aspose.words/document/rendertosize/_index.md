---
title: Document.RenderToSize
linktitle: RenderToSize
articleTitle: RenderToSize
second_title: Aspose.Words för .NET
description: Upptäck RenderToSize-metoden för att effektivt konvertera dokumentsidor till grafikobjekt med önskade dimensioner. Förbättra din renderingsprocess idag!
type: docs
weight: 740
url: /sv/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Återger en dokumentsida till enGraphics objekt till en specificerad storlek.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pageIndex | Int32 | Det 0-baserade sidindexet. |
| graphics | Graphics | Objektet dit det ska renderas. |
| x | Single | X-koordinaten (i världsenheter) för det övre vänstra hörnet av den renderade sidan. |
| y | Single | Y-koordinaten (i världsenheter) för det övre vänstra hörnet av den renderade sidan. |
| width | Single | Den maximala bredden (i världsenheter) som den renderade sidan kan uppta. |
| height | Single | Den maximala höjden (i världsenheter) som den renderade sidan kan uppta. |

### Returvärde

Skalan som automatiskt beräknades för att den renderade sidan skulle passa den angivna storleken.

## Exempel

Visar hur man renderar dokumentet som en bitmapp på en angiven plats och storlek (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Tillämpa en skalningsfaktor på 70 % på sidan som vi ska rendera med hjälp av denna arbetsyta.
        canvas.Scale(70);

        // Förskjut sidan 0,5" från sidans övre och vänstra kanter.
        canvas.Translate(0.5f, 0.5f);

        // Rotera den renderade sidan med 10 grader.
        canvas.RotateDegrees(10);

        // Skapa och rita en rektangel.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Rendera den första sidan av dokumentet till samma storlek som ovanstående rektangel.
        // Rektangeln kommer att rama in den här sidan.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Återställ matrisen och använd sedan en ny uppsättning skalning och översättningar.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // Skapa en annan rektangel.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // Rendera den första sidan inom den nyskapade rektangeln igen.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Visar hur man renderar ett dokument till en bitmapp på en angiven plats och i en angiven storlek.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Ställ in egenskapen "PageUnit" till "GraphicsUnit.Inch" för att använda tum som
        // måttenhet för alla transformationer och dimensioner som vi definierar.
        gr.PageUnit = GraphicsUnit.Inch;

        // Förskjut utgången 0,5" från kanten.
        gr.TranslateTransform(0.5f, 0.5f);

        // Rotera utgången med 10 grader.
        gr.RotateTransform(10);

        // Rita en 3"x3" rektangel.
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Rita den första sidan av vårt dokument med samma dimensioner och transformation som rektangeln.
        // Rektangeln kommer att rama in den första sidan.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Detta är skalningsfaktorn som RenderToSize-metoden tillämpade på den första sidan för att passa den angivna storleken.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Ställ in egenskapen "PageUnit" till "GraphicsUnit.Millimeter" för att använda millimeter som
        // måttenhet för alla transformationer och dimensioner som vi definierar.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Återställer transformationerna som vi använde från föregående rendering.
        gr.ResetTransform();

         // Tillämpa ytterligare en uppsättning transformationer.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Skapa en annan rektangel och använd den för att rama in en annan sida från dokumentet.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
