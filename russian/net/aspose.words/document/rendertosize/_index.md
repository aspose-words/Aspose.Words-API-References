---
title: Document.RenderToSize
second_title: Справочник по API Aspose.Words для .NET
description: Document метод. Преобразует страницу документа вGraphics объект до указанного размера.
type: docs
weight: 670
url: /ru/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Преобразует страницу документа вGraphics объект до указанного размера.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | Int32 | Индекс страницы, начинающийся с 0. |
| graphics | Graphics | Объект, на который выполняется рендеринг. |
| x | Single | Координата X (в мировых единицах) левого верхнего угла отображаемой страницы. |
| y | Single | Координата Y (в мировых единицах) левого верхнего угла отображаемой страницы. |
| width | Single | Максимальная ширина (в мировых единицах), которую может занимать отображаемая страница. |
| height | Single | Максимальная высота (в мировых единицах), которую может занимать отображаемая страница. |

### Возвращаемое значение

Масштаб, который был автоматически рассчитан для отображаемой страницы, чтобы соответствовать указанному размеру.

### Примеры

Показывает, как визуализировать документ в виде растрового изображения в указанном месте и размере (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Применяем коэффициент масштабирования 70% к странице, которую мы будем отображать с использованием этого холста.
        canvas.Scale(70);

        // Сместим страницу на 0,5 дюйма от верхнего и левого краев страницы.
        canvas.Translate(0.5f, 0.5f);

        // Поворот отображаемой страницы на 10 градусов.
        canvas.RotateDegrees(10);

        // Создаем и рисуем прямоугольник.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Рендерим первую страницу документа того же размера, что и прямоугольник выше.
        // Прямоугольник будет обрамлять эту страницу.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Сбросить матрицу, а затем применить новый набор масштабирования и переводов.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // Создаем еще один прямоугольник.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // Визуализируем первую страницу внутри только что созданного прямоугольника еще раз.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Показывает, как преобразовать документ в растровое изображение в указанном месте и размере.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Установите для свойства "PageUnit" значение "GraphicsUnit.Inch", чтобы использовать дюймы в качестве
        // единица измерения для любых преобразований и измерений, которые мы будем определять.
        gr.PageUnit = GraphicsUnit.Inch;

        // Смещение вывода на 0,5 дюйма от края.
        gr.TranslateTransform(0.5f, 0.5f);

        // Повернуть вывод на 10 градусов.
        gr.RotateTransform(10);

        // Рисуем прямоугольник 3"x3".
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Нарисуйте первую страницу нашего документа с теми же размерами и трансформацией, что и прямоугольник.
        // Прямоугольник будет обрамлять первую страницу.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Это коэффициент масштабирования, который метод RenderToSize применил к первой странице, чтобы она соответствовала указанному размеру.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Установите для свойства "PageUnit" значение "GraphicsUnit.Millimeter", чтобы использовать миллиметры в качестве
        // единица измерения для любых преобразований и измерений, которые мы будем определять.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Сбросить преобразования, которые мы использовали из предыдущего рендеринга.
        gr.ResetTransform();

         // Применяем другой набор преобразований.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Создаем еще один прямоугольник и используем его для обрамления другой страницы документа.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


