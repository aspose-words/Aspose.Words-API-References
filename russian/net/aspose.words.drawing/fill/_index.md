---
title: Fill Class
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.Drawing.Fill для расширенных параметров форматирования заливки, которые позволят вам без труда улучшить дизайн и визуальную привлекательность документа.
type: docs
weight: 1270
url: /ru/net/aspose.words.drawing/fill/
---
## Fill class

Представляет форматирование заполнения для объекта.

Чтобы узнать больше, посетите[Работа с графическими элементами](https://docs.aspose.com/words/net/working-with-graphic-elements/) документальная статья.

```csharp
public class Fill
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Возвращает или задает объект Color, представляющий цвет фона для заливки. |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | Возвращает или задает объект ThemeColor, представляющий цвет фона для заливки. |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | Возвращает или задает двойное значение, которое осветляет или затемняет цвет фона. |
| [BaseForeColor](../../aspose.words.drawing/fill/baseforecolor/) { get; } | Получает объект Color, представляющий базовый цвет переднего плана для fill без каких-либо модификаторов. |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | Возвращает или задает объект Color, представляющий цвет переднего плана для заливки. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Получает тип заполнения. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Возвращает или задает объект Color, представляющий цвет переднего плана для заливки. |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | Возвращает или задает объект ThemeColor, представляющий цвет переднего плана для заливки. |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | Возвращает или задает двойное значение, которое осветляет или затемняет цвет переднего плана. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Получает или задает угол градиентной заливки. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Получает коллекцию[`GradientStop`](../gradientstop/) объекты для заливки. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Получает стиль градиента[`GradientStyle`](../gradientstyle/) для заполнения. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Получает вариант градиента[`GradientVariant`](../gradientvariant/) для заполнения. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Получает необработанные байты текстуры или узора заливки. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Возвращает или задает степень непрозрачности указанной заливки в виде значения от 0,0 (прозрачная) до 1,0 (непрозрачная). |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | Получает[`PatternType`](../patterntype/) для заполнения. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | Получает[`PresetTexture`](../presettexture/) для заполнения. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Возвращает или задает, вращается ли заливка вместе с указанным объектом. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Получает или задает выравнивание для заливки текстуры плитки. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Возвращает или задает степень прозрачности указанной заливки в виде значения от 0,0 (непрозрачная) до 1,0 (прозрачная). |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Получает или задает значение, которое`истинный` если форматирование, примененное к этому экземпляру, видимо. |

## Методы

| Имя | Описание |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Устанавливает указанную заливку в виде одноцветного градиента. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(*Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Устанавливает указанную заливку в виде одноцветного градиента, используя указанный цвет. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(*[PatternType](../patterntype/)*) | Устанавливает указанную заливку в соответствии с шаблоном. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(*[PatternType](../patterntype/), Color, Color*) | Устанавливает указанную заливку в соответствии с шаблоном. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(*[PresetTexture](../presettexture/)*) | Устанавливает заливку на основе предустановленной текстуры. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(*byte[]*) | Изменяет тип заливки на одиночное изображение. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(*Stream*) | Изменяет тип заливки на одиночное изображение. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(*string*) | Изменяет тип заливки на одиночное изображение. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Устанавливает однородный цвет заливки. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(*Color*) | Устанавливает заливку указанным однородным цветом. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Устанавливает указанную заливку в виде двухцветного градиента. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(*Color, Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Устанавливает указанную заливку в виде двухцветного градиента. |

## Примечания

Используйте[`Fill`](../shapebase/fill/) или[`Fill`](../../aspose.words/font/fill/) свойство для доступа к свойствам заполнения объекта. Вы не создаете экземпляры`Fill` класс напрямую.

## Примеры

Показывает, как залить фигуру сплошным цветом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Напишите текст, а затем закройте его плавающей фигурой.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Используйте свойство "StrokeColor", чтобы задать цвет контура фигуры.
shape.StrokeColor = Color.CadetBlue;

// Используйте свойство «FillColor», чтобы задать цвет внутренней области фигуры.
shape.FillColor = Color.LightBlue;

// Свойство «Непрозрачность» определяет прозрачность цвета по шкале от 0 до 1,
// где 1 — полностью непрозрачный, а 0 — невидимый.
// Заливка фигуры по умолчанию полностью непрозрачна, поэтому мы не можем видеть текст, над которым находится эта фигура.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Установите меньшее значение непрозрачности цвета заливки фигуры, чтобы мы могли видеть текст под ней.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
