---
title: TextBox Class
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.TextBox сорт. Определяет атрибуты которые определяют как текст отображается внутри фигуры на С#.
type: docs
weight: 1320
url: /ru/net/aspose.words.drawing/textbox/
---
## TextBox class

Определяет атрибуты, которые определяют, как текст отображается внутри фигуры.

Чтобы узнать больше, посетите[Работа с фигурами](https://docs.aspose.com/words/net/working-with-shapes/) статья документации.

```csharp
public class TextBox
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | Определяет, будет ли Microsoft Word увеличивать форму до размера текста. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | Определяет внутреннее нижнее поле фигуры в пунктах. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | Определяет внутреннее левое поле фигуры в пунктах. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | Определяет внутреннее правое поле фигуры в пунктах. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | Определяет внутреннее верхнее поле фигуры в пунктах. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | Определяет расположение текста в фигуре. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | Возвращает или устанавливает`TextBox` который представляет собой следующий`TextBox` в последовательности фигур. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | Получает или задает логическое значение, указывающее, что текст TextBox не должен вращаться при повороте фигуры. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | Получает родительскую фигуру для`TextBox` . |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | Возвращает`TextBox` который представляет собой предыдущий`TextBox` в последовательности фигур. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | Определяет, как текст переносится внутри фигуры. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | Определяет вертикальное выравнивание текста внутри фигуры. |

## Методы

| Имя | Описание |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | Разрывает ссылку на следующий`TextBox` . |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | Определяет, является ли это`TextBox` может быть привязан к цели`TextBox` . |

## Примечания

Использовать[`TextBox`](../shape/textbox/) свойство для доступа к текстовым свойствам фигуры. Вы не создаете экземпляры`TextBox` класс напрямую.

## Примеры

Показывает, как установить внутренние поля для текстового поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем еще одно текстовое поле с определенными полями.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

Показывает, как задать ориентацию текста внутри текстового поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Переместите конструктор документов внутрь TextBox и добавьте текст.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Установите свойство LayoutFlow, чтобы задать ориентацию текстового содержимого этого текстового поля.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

Показывает, как изменить размер текстового поля, чтобы оно плотно вписывалось в его содержимое.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Применяем эти значения к обоим элементам, чтобы родительская фигура соответствовала размеру
// плотно окружает текстовое содержимое, игнорируя установленные нами размеры.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
