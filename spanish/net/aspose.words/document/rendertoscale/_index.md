---
title: Document.RenderToScale
linktitle: RenderToScale
articleTitle: RenderToScale
second_title: Aspose.Words para .NET
description: Descubra el método RenderToScale para renderizar de manera eficiente páginas de documentos en objetos gráficos en la escala deseada para obtener resultados visuales óptimos.
type: docs
weight: 730
url: /es/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

Representa una página de documento en unGraphics objeto a una escala especificada.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pageIndex | Int32 | El índice de página basado en 0. |
| graphics | Graphics | El objeto donde renderizar. |
| x | Single | La coordenada X (en unidades mundiales) de la esquina superior izquierda de la página renderizada. |
| y | Single | La coordenada Y (en unidades mundiales) de la esquina superior izquierda de la página renderizada. |
| scale | Single | La escala para renderizar la página (1.0 es 100%). |

### Valor_devuelto

El ancho y la altura (en unidades mundiales) de la página renderizada.

## Ejemplos

Muestra cómo convertir las páginas individuales de un documento en gráficos para crear una imagen con miniaturas de todas las páginas.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Calcula el número de filas y columnas que llenaremos con miniaturas.
const int thumbColumns = 2;
int thumbRows = doc.PageCount / thumbColumns;
int remainder = doc.PageCount % thumbColumns;

if (remainder > 0)
    thumbRows++;

// Escala las miniaturas en relación con el tamaño de la primera página.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Calcula el tamaño de la imagen que contendrá todas las miniaturas.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Rellena el fondo, que es transparente por defecto, en blanco.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbColumns;
            int columnIdx = pageIndex % thumbColumns;

            // Especifica dónde queremos que aparezca la miniatura.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // Representa una página como miniatura y luego enmárcala en un rectángulo del mismo tamaño.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

Convierte páginas individuales en gráficos para crear una imagen con miniaturas de todas las páginas (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Calcula el número de filas y columnas que llenaremos con miniaturas.
const int thumbnailColumnsNum = 2;
int thumbRows = doc.PageCount / thumbnailColumnsNum;
int remainder = doc.PageCount % thumbnailColumnsNum;

if (remainder > 0)
    thumbRows++;

 // Escala las miniaturas en relación con el tamaño de la primera página.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Calcula el tamaño de la imagen que contendrá todas las miniaturas.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Rellena el fondo, que es transparente por defecto, en blanco.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbnailColumnsNum;
            int columnIdx = pageIndex % thumbnailColumnsNum;

            // Especifica dónde queremos que aparezca la miniatura.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // Representa una página como miniatura y luego enmárcala en un rectángulo del mismo tamaño.
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

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
