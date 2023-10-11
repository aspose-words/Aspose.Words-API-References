---
title: Document.RenderToSize
second_title: Справочник по API Aspose.Words для .NET
description: Document метод. Преобразует страницу документа вGraphics объект указанного размера.
type: docs
weight: 710
url: /ru/net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Преобразует страницу документа вGraphics объект указанного размера.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | Int32 | Индекс страницы, отсчитываемый от 0. |
| graphics | Graphics | Объект, в который выполняется рендеринг. |
| x | Single | Координата X (в мировых единицах измерения) верхнего левого угла отображаемой страницы. |
| y | Single | Координата Y (в мировых единицах измерения) верхнего левого угла отображаемой страницы. |
| width | Single | Максимальная ширина (в мировых единицах), которую может занимать отображаемая страница. |
| height | Single | Максимальная высота (в мировых единицах), которую может занимать отображаемая страница. |

### Возвращаемое значение

Масштаб, который автоматически рассчитывается для отображаемой страницы в соответствии с указанным размером.

### Примеры

Показывает, как визуализировать документ в виде растрового изображения в указанном месте и размере (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Примените коэффициент масштабирования 70 % к странице, которую мы будем отображать с помощью этого холста.
        canvas.Scale(70);

        // Смещаем страницу на 0,5 дюйма от верхнего и левого краев страницы.
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

        // Рендеринг первой страницы документа до того же размера, что и прямоугольник выше.
        // Прямоугольник будет обрамлять эту страницу.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Сбрасываем матрицу, а затем применяем новый набор масштабирования и преобразований.
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

        // Снова визуализируем первую страницу внутри вновь созданного прямоугольника.
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

        // Установите для свойства «PageUnit» значение «GraphicsUnit.Inch», чтобы использовать дюймы в качестве
        // единица измерения для любых преобразований и размеров, которые мы определим.
        gr.PageUnit = GraphicsUnit.Inch;

        // Смещаем вывод на 0,5 дюйма от края.
        gr.TranslateTransform(0.5f, 0.5f);

        // Поворот вывода на 10 градусов.
        gr.RotateTransform(10);

        // Рисуем прямоугольник размером 3х3 дюйма.
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Нарисуйте первую страницу нашего документа с теми же размерами и преобразованием, что и прямоугольник.
        // Прямоугольник будет обрамлять первую страницу.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // Это коэффициент масштабирования, который метод RenderToSize применил к первой странице, чтобы она соответствовала указанному размеру.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Установите для свойства «PageUnit» значение «GraphicsUnit.Millimeter», чтобы использовать миллиметры в качестве
        // единица измерения для любых преобразований и размеров, которые мы определим.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Сбрасываем преобразования, которые мы использовали при предыдущем рендеринге.
        gr.ResetTransform();

        // Применяем другой набор преобразований.
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Создаем еще один прямоугольник и используем его для рамки другой страницы документа.
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


