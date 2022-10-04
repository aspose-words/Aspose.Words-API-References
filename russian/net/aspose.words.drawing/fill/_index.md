---
title: Fill
second_title: Справочник по API Aspose.Words для .NET
description: Представляет форматирование заливки для объекта.
type: docs
weight: 820
url: /ru/net/aspose.words.drawing/fill/
---
## Fill class

Представляет форматирование заливки для объекта.

```csharp
public class Fill
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Получает или задает объект Color, представляющий цвет фона для заливки. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Получает тип заливки. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Получает или задает объект Color, представляющий цвет переднего плана для заливки. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Получает или задает угол градиентной заливки. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Получает коллекцию[`GradientStop`](../gradientstop/) объекты для заливки. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Получает стиль градиента[`GradientStyle`](../gradientstyle/) для заливки. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Получает вариант градиента[`GradientVariant`](../gradientvariant/) для заливки. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Получает необработанные байты текстуры или узора заливки. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Получает или задает степень непрозрачности указанной заливки в виде значения от 0,0 (прозрачная) до 1,0 (непрозрачная). |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | Получает[`PatternType`](../patterntype/) для заливки. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | Получает[`PresetTexture`](../presettexture/) для заливки. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Получает или задает, вращается ли заливка с указанным объектом. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Получает или задает выравнивание для заливки текстурой тайла. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Получает или задает степень прозрачности указанной заливки в виде значения от 0,0 (непрозрачная) до 1,0 (прозрачная). |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Получает или задает значение, которое`истинный` если форматирование, примененное к этому экземпляру, видимо. |

## Методы

| Имя | Описание |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(GradientStyle, GradientVariant, double) | Задает для указанной заливки одноцветный градиент. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(Color, GradientStyle, GradientVariant, double) | Задает для указанной заливки одноцветный градиент с использованием указанного цвета. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(PatternType) | Устанавливает указанную заливку в шаблон. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(PatternType, Color, Color) | Устанавливает указанную заливку в шаблон. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(PresetTexture) | Задает заливку предустановленной текстурой. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(byte[]) | Изменяет тип заливки на одно изображение. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(Stream) | Изменяет тип заливки на одно изображение. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(string) | Изменяет тип заливки на одно изображение. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Устанавливает заливку однородным цветом. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(Color) | Устанавливает заливку указанным однородным цветом. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(GradientStyle, GradientVariant) | Устанавливает для указанной заливки двухцветный градиент. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(Color, Color, GradientStyle, GradientVariant) | Устанавливает для указанной заливки двухцветный градиент. |

### Примечания

Использовать[`Fill`](../shapebase/fill/) или же[`Fill`](../../aspose.words/font/fill/) свойство для доступа к свойствам заливки объекта. Вы не создаете экземпляры[`Fill`](./fill/) класс напрямую.

### Примеры

Показывает, как заполнить фигуру сплошным цветом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Напишите какой-нибудь текст, а затем накройте его плавающей фигурой.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Используйте свойство "StrokeColor", чтобы установить цвет контура фигуры.
shape.StrokeColor = Color.CadetBlue;

// Используйте свойство "FillColor", чтобы задать цвет внутренней области фигуры.
shape.FillColor = Color.LightBlue;

// Свойство "Непрозрачность" определяет, насколько прозрачен цвет по шкале от 0 до 1,
// где 1 полностью непрозрачно, а 0 невидимо.
// Заливка фигуры по умолчанию полностью непрозрачна, поэтому мы не можем видеть текст, поверх которого находится эта фигура.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Установите непрозрачность цвета заливки фигуры на более низкое значение, чтобы мы могли видеть текст под ним.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
