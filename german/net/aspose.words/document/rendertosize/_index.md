---
title: Document.RenderToSize
linktitle: RenderToSize
articleTitle: RenderToSize
second_title: Aspose.Words für .NET
description: Entdecken Sie die RenderToSize-Methode, um Dokumentseiten effizient in Grafikobjekte in den gewünschten Abmessungen umzuwandeln. Optimieren Sie Ihren Rendering-Prozess noch heute!
type: docs
weight: 740
url: /de/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Rendert eine Dokumentseite in eineGraphics Objekt auf eine angegebene Größe.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageIndex | Int32 | Der 0-basierte Seitenindex. |
| graphics | Graphics | Das Objekt, in das gerendert werden soll. |
| x | Single | Die X-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| y | Single | Die Y-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| width | Single | Die maximale Breite (in Welteinheiten), die von der gerenderten Seite eingenommen werden kann. |
| height | Single | Die maximale Höhe (in Welteinheiten), die von der gerenderten Seite eingenommen werden kann. |

### Rückgabewert

Der Maßstab, der automatisch berechnet wurde, damit die gerenderte Seite der angegebenen Größe entspricht.

## Beispiele

Zeigt, wie das Dokument als Bitmap an einer angegebenen Position und in einer angegebenen Größe gerendert wird (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Wenden Sie einen Skalierungsfaktor von 70 % auf die Seite an, die wir mit dieser Leinwand rendern werden.
        canvas.Scale(70);

        // Versetzen Sie die Seite 0,5 Zoll vom oberen und linken Rand der Seite.
        canvas.Translate(0.5f, 0.5f);

        // Drehen Sie die gerenderte Seite um 10 Grad.
        canvas.RotateDegrees(10);

        // Erstellen und zeichnen Sie ein Rechteck.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Rendern Sie die erste Seite des Dokuments in der gleichen Größe wie das obige Rechteck.
        // Das Rechteck wird diese Seite umrahmen.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Setzen Sie die Matrix zurück und wenden Sie dann einen neuen Satz von Skalierungen und Übersetzungen an.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // Ein weiteres Rechteck erstellen.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // Rendern Sie die erste Seite innerhalb des neu erstellten Rechtecks noch einmal.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Zeigt, wie ein Dokument an einer angegebenen Position und in einer angegebenen Größe in ein Bitmap gerendert wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Setzen Sie die Eigenschaft "PageUnit" auf "GraphicsUnit.Inch", um Zoll als
        // Maßeinheit für alle Transformationen und Dimensionen, die wir definieren.
        gr.PageUnit = GraphicsUnit.Inch;

        // Versetzen Sie die Ausgabe 0,5 Zoll vom Rand.
        gr.TranslateTransform(0.5f, 0.5f);

        // Drehen Sie die Ausgabe um 10 Grad.
        gr.RotateTransform(10);

        // Zeichnen Sie ein 3 x 3 Zoll großes Rechteck.
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Zeichnen Sie die erste Seite unseres Dokuments mit denselben Abmessungen und derselben Transformation wie das Rechteck.
        // Das Rechteck umrahmt die erste Seite.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Dies ist der Skalierungsfaktor, den die Methode RenderToSize auf die erste Seite angewendet hat, um sie an die angegebene Größe anzupassen.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Setzen Sie die Eigenschaft "PageUnit" auf "GraphicsUnit.Millimeter", um Millimeter als
        // Maßeinheit für alle Transformationen und Dimensionen, die wir definieren.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Setzen Sie die Transformationen zurück, die wir beim vorherigen Rendering verwendet haben.
        gr.ResetTransform();

            // Einen weiteren Satz Transformationen anwenden.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Erstellen Sie ein weiteres Rechteck und verwenden Sie es, um eine weitere Seite des Dokuments einzurahmen.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
