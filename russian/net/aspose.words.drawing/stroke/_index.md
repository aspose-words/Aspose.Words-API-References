---
title: Stroke Class
linktitle: Stroke
articleTitle: Stroke
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Stroke, чтобы улучшить свои фигуры с помощью настраиваемых штрихов, без труда добавив профессиональный вид вашим документам.
type: docs
weight: 1720
url: /ru/net/aspose.words.drawing/stroke/
---
## Stroke class

Определяет обводку для фигуры.

Чтобы узнать больше, посетите[Работа с фигурами](https://docs.aspose.com/words/net/working-with-shapes/) документальная статья.

```csharp
public class Stroke
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor/) { get; set; } | Получает или задает цвет фона штриха. |
| [BackThemeColor](../../aspose.words.drawing/stroke/backthemecolor/) { get; set; } | Возвращает или задает объект ThemeColor, представляющий цвет фона обводки. |
| [BackTintAndShade](../../aspose.words.drawing/stroke/backtintandshade/) { get; set; } | Возвращает или задает двойное значение, которое осветляет или затемняет цвет фона обводки. |
| [BaseForeColor](../../aspose.words.drawing/stroke/baseforecolor/) { get; } | Получает базовый цвет переднего плана обводки без каких-либо модификаторов. |
| [Color](../../aspose.words.drawing/stroke/color/) { get; set; } | Определяет цвет обводки. |
| [Color2](../../aspose.words.drawing/stroke/color2/) { get; set; } | Определяет второй цвет для обводки. |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle/) { get; set; } | Задает шаблон точек и тире для штриха. |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength/) { get; set; } | Определяет длину наконечника стрелки в конце штриха. |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype/) { get; set; } | Определяет наконечник стрелки для конца штриха. |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth/) { get; set; } | Определяет ширину наконечника стрелки в конце штриха. |
| [EndCap](../../aspose.words.drawing/stroke/endcap/) { get; set; } | Определяет стиль окончания штриха. |
| [Fill](../../aspose.words.drawing/stroke/fill/) { get; } | Получает форматирование заполнения для`Stroke` . |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor/) { get; set; } | Получает или задает цвет переднего плана штриха. |
| [ForeThemeColor](../../aspose.words.drawing/stroke/forethemecolor/) { get; set; } | Возвращает или задает объект ThemeColor, представляющий цвет переднего плана обводки. |
| [ForeTintAndShade](../../aspose.words.drawing/stroke/foretintandshade/) { get; set; } | Возвращает или задает двойное значение, которое осветляет или затемняет цвет переднего плана обводки. |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes/) { get; } | Определяет изображение для штрихового изображения или узорной заливки. |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle/) { get; set; } | Определяет стиль соединения полилинии. |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle/) { get; set; } | Определяет стиль линии штриха. |
| [On](../../aspose.words.drawing/stroke/on/) { get; set; } | Определяет, будет ли контур обведен. |
| [Opacity](../../aspose.words.drawing/stroke/opacity/) { get; set; } | Определяет степень прозрачности штриха. Допустимый диапазон от 0 до 1. |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength/) { get; set; } | Определяет длину наконечника стрелки для начала штриха. |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype/) { get; set; } | Определяет наконечник стрелки для начала штриха. |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth/) { get; set; } | Определяет ширину наконечника стрелки для начала штриха. |
| [Transparency](../../aspose.words.drawing/stroke/transparency/) { get; set; } | Возвращает или задает значение от 0,0 (непрозрачный) до 1,0 (прозрачный), представляющее степень прозрачности штриха. |
| [Visible](../../aspose.words.drawing/stroke/visible/) { get; set; } | Возвращает или задает флаг, указывающий, видима ли обводка. |
| [Weight](../../aspose.words.drawing/stroke/weight/) { get; set; } | Определяет толщину кисти, обводящей контур фигуры, в точках. |

## Примечания

Используйте[`Stroke`](../shape/stroke/)свойство для доступа к свойствам штриха фигуры. Вы не создаете экземпляры`Stroke` класс напрямую.

## Примеры

Показывает, как изменить свойства штриха.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Базовые фигуры, такие как прямоугольник, состоят из двух видимых частей.
// 1 — Заливка, которая применяется к области внутри контура фигуры:
shape.Fill.ForeColor = Color.White;

// 2 - Штрих, обозначающий контур фигуры:
// Измените различные свойства обводки этой фигуры.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
