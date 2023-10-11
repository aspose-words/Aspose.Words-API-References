---
title: Document.RenderToSize
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. Representa una página de documento en unGraphics objeto a un tamaño específico.
type: docs
weight: 710
url: /es/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Representa una página de documento en unGraphics objeto a un tamaño específico.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pageIndex | Int32 | El índice de página basado en 0. |
| graphics | Graphics | El objeto donde renderizar. |
| x | Single | La coordenada X (en unidades mundiales) de la esquina superior izquierda de la página renderizada. |
| y | Single | La coordenada Y (en unidades mundiales) de la esquina superior izquierda de la página renderizada. |
| width | Single | El ancho máximo (en unidades mundiales) que puede ocupar la página renderizada. |
| height | Single | La altura máxima (en unidades mundiales) que puede ocupar la página renderizada. |

### Valor_devuelto

La escala que se calculó automáticamente para que la página renderizada se ajustara al tamaño especificado.

### Ejemplos

Muestra cómo representar el documento como un mapa de bits en una ubicación y tamaño específicos (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Aplicar un factor de escala del 70% a la página que representaremos usando este lienzo.
        canvas.Scale(70);

        // Desplaza la página 0,5" desde los bordes superior e izquierdo de la página.
        canvas.Translate(0.5f, 0.5f);

        // Gira la página renderizada 10 grados.
        canvas.RotateDegrees(10);

        // Crea y dibuja un rectángulo.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Representa la primera página del documento al mismo tamaño que el rectángulo anterior.
        // El rectángulo enmarcará esta página.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Restablece la matriz y luego aplica un nuevo conjunto de escalas y traducciones.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // Crea otro rectángulo.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // Representa nuevamente la primera página dentro del rectángulo recién creado.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Muestra cómo representar un documento en un mapa de bits en una ubicación y tamaño específicos.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Establece la propiedad "PageUnit" en "GraphicsUnit.Inch" para usar pulgadas como tamaño
        // unidad de medida para cualquier transformación y dimensión que definamos.
        gr.PageUnit = GraphicsUnit.Inch;

        // Compensa la salida 0,5" desde el borde.
        gr.TranslateTransform(0.5f, 0.5f);

        // Gira la salida 10 grados.
        gr.RotateTransform(10);

        // Dibuja un rectángulo de 3"x3".
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Dibuja la primera página de nuestro documento con las mismas dimensiones y transformación que el rectángulo.
        // El rectángulo enmarcará la primera página.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Este es el factor de escala que el método RenderToSize aplicó a la primera página para ajustarse al tamaño especificado.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Establece la propiedad "PageUnit" en "GraphicsUnit.Millimeter" para usar milímetros como
        // unidad de medida para cualquier transformación y dimensión que definamos.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Restablece las transformaciones que usamos en el renderizado anterior.
        gr.ResetTransform();

        // Aplicar otro conjunto de transformaciones.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Crea otro rectángulo y úsalo para enmarcar otra página del documento.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


