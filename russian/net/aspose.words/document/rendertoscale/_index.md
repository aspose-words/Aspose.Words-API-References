---
title: Document.RenderToScale
second_title: Справочник по API Aspose.Words для .NET
description: Document метод. Преобразует страницу документа вGraphics объект в указанном масштабе.
type: docs
weight: 700
url: /ru/net/aspose.words/document/rendertoscale/
---
## Document.RenderToScale method

Преобразует страницу документа вGraphics объект в указанном масштабе.

```csharp
public SizeF RenderToScale(int pageIndex, Graphics graphics, float x, float y, float scale)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | Int32 | Индекс страницы, отсчитываемый от 0. |
| graphics | Graphics | Объект, в который выполняется рендеринг. |
| x | Single | Координата X (в мировых единицах измерения) верхнего левого угла отображаемой страницы. |
| y | Single | Координата Y (в мировых единицах измерения) верхнего левого угла отображаемой страницы. |
| scale | Single | Масштаб отрисовки страницы (1.0 — 100%). |

### Возвращаемое значение

Ширина и высота (в мировых единицах) отображаемой страницы.

### Примеры

Показывает, как из отдельных страниц документа с графикой создать одно изображение с миниатюрами всех страниц.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Подсчитаем количество строк и столбцов, которые мы заполним миниатюрами.
const int thumbColumns = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbColumns, out int remainder);

if (remainder > 0)
    thumbRows++;

// Масштабируем миниатюры относительно размера первой страницы.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Вычисляем размер изображения, которое будет содержать все миниатюры.
int imgWidth = thumbSize.Width * thumbColumns;
int imgHeight = thumbSize.Height * thumbRows;

using (Bitmap img = new Bitmap(imgWidth, imgHeight))
{
    using (Graphics gr = Graphics.FromImage(img))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Заливаем фон, который по умолчанию прозрачный, белым.
        gr.FillRectangle(new SolidBrush(Color.White), 0, 0, imgWidth, imgHeight);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbColumns, out int columnIdx);

            // Указываем, где мы хотим, чтобы миниатюра отображалась.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            // Отрисовываем страницу как миниатюру, а затем обрамляем ее прямоугольником того же размера.
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

// Подсчитаем количество строк и столбцов, которые мы заполним миниатюрами.
const int thumbnailColumnsNum = 2;
int thumbRows = Math.DivRem(doc.PageCount, thumbnailColumnsNum, out int remainder);

if (remainder > 0)
    thumbRows++;

 // Масштабируем миниатюры относительно размера первой страницы.
const float scale = 0.25f;
Size thumbSize = doc.GetPageInfo(0).GetSizeInPixels(scale, 96);

// Вычисляем размер изображения, которое будет содержать все миниатюры.
int imgWidth = thumbSize.Width * thumbnailColumnsNum;
int imgHeight = thumbSize.Height * thumbRows;

using (SKBitmap bitmap = new SKBitmap(imgWidth, imgHeight))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Заливаем фон, который по умолчанию прозрачный, белым.
        canvas.Clear(SKColors.White);

        for (int pageIndex = 0; pageIndex < doc.PageCount; pageIndex++)
        {
            int rowIdx = Math.DivRem(pageIndex, thumbnailColumnsNum, out int columnIdx);

            // Указываем, где мы хотим, чтобы миниатюра отображалась.
            float thumbLeft = columnIdx * thumbSize.Width;
            float thumbTop = rowIdx * thumbSize.Height;

            SizeF size = doc.RenderToScale(pageIndex, canvas, thumbLeft, thumbTop, scale);

            // Отрисовываем страницу как миниатюру, а затем обрамляем ее прямоугольником того же размера.
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
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


