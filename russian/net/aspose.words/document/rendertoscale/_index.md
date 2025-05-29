---
title: Document.RenderToScale
linktitle: RenderToScale
articleTitle: RenderToScale
second_title: Aspose.Words для .NET
description: Откройте для себя метод RenderToScale для эффективного преобразования страниц документов в графические объекты в желаемом масштабе для достижения оптимальных визуальных результатов.
type: docs
weight: 730
url: /ru/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

Преобразует страницу документа вGraphics объект в указанном масштабе.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | Int32 | Индекс страниц, начинающийся с 0. |
| graphics | Graphics | Объект, куда будет осуществляться рендеринг. |
| x | Single | Координата X (в мировых единицах) верхнего левого угла отображаемой страницы. |
| y | Single | Координата Y (в мировых единицах) верхнего левого угла отображаемой страницы. |
| scale | Single | Масштаб отображения страницы (1,0 = 100%). |

### Возвращаемое значение

Ширина и высота (в мировых единицах) отображаемой страницы.

## Примеры

Показывает, как преобразовать отдельные страницы документа в графику, чтобы создать одно изображение с миниатюрами всех страниц.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Рассчитаем количество строк и столбцов, которые мы заполним миниатюрами.
const int thumbColumns = 2;
int thumbRows = doc.PageCount / thumbColumns;
int remainder = doc.PageCount % thumbColumns;

if (remainder > 0)
    thumbRows++;

// Масштабировать миниатюры относительно размера первой страницы.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Рассчитаем размер изображения, которое будет содержать все миниатюры.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Заполняем фон, который по умолчанию прозрачен, белым цветом.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbColumns;
            int columnIdx = pageIndex % thumbColumns;

            // Укажите, где мы хотим видеть миниатюру.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // Отобразить страницу в виде миниатюры, а затем поместить ее в прямоугольник того же размера.
            SizeF size = doc.RenderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);
            gr.DrawRectangle(Pens.Black, thumbLeft, thumbTop, size.Width, size.Height);
        }

        img.Save(ArtifactsDir + "Rendering.Thumbnails.png");
    }
}
```

Преобразует отдельные страницы в графику для создания одного изображения с миниатюрами всех страниц (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Рассчитаем количество строк и столбцов, которые мы заполним миниатюрами.
const int thumbnailColumnsNum = 2;
int thumbRows = doc.PageCount / thumbnailColumnsNum;
int remainder = doc.PageCount % thumbnailColumnsNum;

if (remainder > 0)
    thumbRows++;

 // Масштабировать миниатюры относительно размера первой страницы.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Рассчитаем размер изображения, которое будет содержать все миниатюры.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Заполняем фон, который по умолчанию прозрачен, белым цветом.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = pageIndex / thumbnailColumnsNum;
            int columnIdx = pageIndex % thumbnailColumnsNum;

            // Укажите, где мы хотим видеть миниатюру.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // Отобразить страницу в виде миниатюры, а затем поместить ее в прямоугольник того же размера.
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

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
