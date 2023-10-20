---
title: Document.RenderToSize
linktitle: RenderToSize
articleTitle: RenderToSize
second_title: Aspose.Words für .NET
description: Document RenderToSize methode. Rendert eine Dokumentseite in eineGraphics Objekt auf eine angegebene Größe in C#.
type: docs
weight: 690
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
| graphics | Graphics | Das Objekt, zu dem gerendert werden soll. |
| x | Single | Die X-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| y | Single | Die Y-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Seite. |
| width | Single | Die maximale Breite (in Welteinheiten), die von der gerenderten Seite eingenommen werden kann. |
| height | Single | Die maximale Höhe (in Welteinheiten), die von der gerenderten Seite eingenommen werden kann. |

### Rückgabewert

Der Maßstab, der automatisch für die gerenderte Seite berechnet wurde, damit sie der angegebenen Größe entspricht.

## Beispiele

Zeigt, wie das Dokument als Bitmap an einer angegebenen Position und Größe gerendert wird (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Wenden Sie einen Skalierungsfaktor von 70 % auf die Seite an, die wir mit dieser Leinwand rendern werden.
        canvas.Scale(70);

        // Versetze die Seite um 0,5 Zoll vom oberen und linken Rand der Seite.
        canvas.Translate(0.5f, 0.5f);

        // Die gerenderte Seite um 10 Grad drehen.
        canvas.RotateDegrees(10);

        // Erstelle und zeichne ein Rechteck.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Rendern Sie die erste Seite des Dokuments auf die gleiche Größe wie das obige Rechteck.
        // Das Rechteck umrahmt diese Seite.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Setzen Sie die Matrix zurück und wenden Sie dann einen neuen Satz von Skalierungen und Übersetzungen an.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // Erstelle ein weiteres Rechteck.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // Die erste Seite innerhalb des neu erstellten Rechtecks noch einmal rendern.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Zeigt, wie ein Dokument an einer bestimmten Position und Größe in eine Bitmap gerendert wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Setzen Sie die Eigenschaft „PageUnit“ auf „GraphicsUnit.Inch“, um Zoll als zu verwenden
        // Maßeinheit für alle Transformationen und Dimensionen, die wir definieren.
        gr.PageUnit = GraphicsUnit.Inch;

        // Versetze die Ausgabe um 0,5 Zoll vom Rand.
        gr.TranslateTransform(0.5f, 0.5f);

        // Ausgabe um 10 Grad drehen.
        gr.RotateTransform(10);

        // Zeichne ein 3 x 3 Zoll großes Rechteck.
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Zeichnen Sie die erste Seite unseres Dokuments mit den gleichen Abmessungen und der gleichen Transformation wie das Rechteck.
        // Das Rechteck umrahmt die erste Seite.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Dies ist der Skalierungsfaktor, den die RenderToSize-Methode auf die erste Seite anwendet, um sie an die angegebene Größe anzupassen.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Setzen Sie die Eigenschaft „PageUnit“ auf „GraphicsUnit.Millimeter“, um Millimeter als zu verwenden
        // Maßeinheit für alle Transformationen und Dimensionen, die wir definieren.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Setzt die Transformationen zurück, die wir aus dem vorherigen Rendering verwendet haben.
        gr.ResetTransform();

        // Einen weiteren Satz Transformationen anwenden.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Erstelle ein weiteres Rechteck und verwende es, um eine weitere Seite aus dem Dokument einzurahmen.
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
