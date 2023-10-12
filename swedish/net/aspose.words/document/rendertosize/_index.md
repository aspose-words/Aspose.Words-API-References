---
title: Document.RenderToSize
second_title: Aspose.Words för .NET API Referens
description: Document metod. Gör en dokumentsida till enGraphics objekt till en angiven storlek.
type: docs
weight: 710
url: /sv/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Gör en dokumentsida till enGraphics objekt till en angiven storlek.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pageIndex | Int32 | Det 0-baserade sidindexet. |
| graphics | Graphics | Objektet där det ska renderas. |
| x | Single | X-koordinaten (i världsenheter) i det övre vänstra hörnet på den renderade sidan. |
| y | Single | Y-koordinaten (i världsenheter) i det övre vänstra hörnet på den renderade sidan. |
| width | Single | Den maximala bredd (i världsenheter) som kan upptas av den renderade sidan. |
| height | Single | Den maximala höjden (i världsenheter) som kan upptas av den renderade sidan. |

### Returvärde

Skalan som automatiskt beräknades för den renderade sidan för att passa den angivna storleken.

### Exempel

Visar hur man renderar dokumentet som en bitmapp på en angiven plats och storlek (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Tillämpa en skalningsfaktor på 70 % på sidan som vi kommer att rendera med den här arbetsytan.
        canvas.Scale(70);

        // Förskjut sidan 0,5" från sidans övre och vänstra kanter.
        canvas.Translate(0.5f, 0.5f);

        // Rotera den renderade sidan 10 grader.
        canvas.RotateDegrees(10);

        // Skapa och rita en rektangel.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Gör den första sidan i dokumentet till samma storlek som rektangeln ovan.
        // Rektangeln kommer att rama in den här sidan.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Återställ matrisen och använd sedan en ny uppsättning skalning och översättningar.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // Skapa ytterligare en rektangel.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // Gör den första sidan i den nyskapade rektangeln igen.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Visar hur man renderar ett dokument till en bitmapp på en angiven plats och storlek.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Ställ in egenskapen "PageUnit" till "GraphicsUnit.Inch" för att använda tum som
        // måttenhet för eventuella transformationer och dimensioner som vi kommer att definiera.
        gr.PageUnit = GraphicsUnit.Inch;

        // Förskjut utgången 0,5" från kanten.
        gr.TranslateTransform(0.5f, 0.5f);

        // Rotera utgången med 10 grader.
        gr.RotateTransform(10);

        // Rita en 3"x3" rektangel.
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Rita första sidan i vårt dokument med samma mått och transformation som rektangeln.
        // Rektangeln kommer att rama in den första sidan.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Detta är skalningsfaktorn som RenderToSize-metoden tillämpade på den första sidan för att passa den angivna storleken.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Ställ in egenskapen "PageUnit" till "GraphicsUnit.Millimeter" för att använda millimeter som
        // måttenhet för eventuella transformationer och dimensioner som vi kommer att definiera.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Återställ transformationerna som vi använde från föregående rendering.
        gr.ResetTransform();

        // Använd en annan uppsättning transformationer.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Skapa ytterligare en rektangel och använd den för att rama in ytterligare en sida från dokumentet.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


