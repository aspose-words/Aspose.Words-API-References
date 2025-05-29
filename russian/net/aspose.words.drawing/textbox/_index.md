---
title: TextBox Class
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.TextBox, который позволяет легко настраивать отображение текста внутри фигур, улучшая визуальную привлекательность и функциональность вашего документа.
type: docs
weight: 1730
url: /ru/net/aspose.words.drawing/textbox/
---
## TextBox class

Определяет атрибуты, которые указывают, как текст отображается внутри фигуры.

Чтобы узнать больше, посетите[Работа с фигурами](https://docs.aspose.com/words/net/working-with-shapes/) документальная статья.

```csharp
public class TextBox
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | Определяет, будет ли Microsoft Word увеличивать фигуру, чтобы вместить текст. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | Указывает внутреннее нижнее поле в пунктах для фигуры. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | Указывает внутреннее левое поле в пунктах для фигуры. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | Указывает внутреннее правое поле в пунктах для фигуры. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | Указывает внутреннее верхнее поле в пунктах для фигуры. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | Определяет поток текста в макете фигуры. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | Возвращает или устанавливает`TextBox` который представляет собой следующий`TextBox`в последовательности фигур. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | Возвращает или задает логическое значение, указывающее, что текст TextBox не должен вращаться при повороте фигуры. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | Получает родительскую форму для`TextBox` . |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | Возвращает`TextBox` который представляет предыдущий`TextBox`в последовательности фигур. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | Определяет, как текст обтекает фигуру. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | Задает вертикальное выравнивание текста внутри фигуры. |

## Методы

| Имя | Описание |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | Разрывает ссылку на следующий`TextBox` . |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | Определяет, является ли это`TextBox` может быть связан с целью`TextBox` . |

## Примечания

Используйте[`TextBox`](../shape/textbox/) свойство для доступа к текстовым свойствам фигуры. Вы не создаете экземпляры`TextBox` класс напрямую.

## Примеры

Показывает, как установить внутренние поля для текстового поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте еще одно текстовое поле с определенными полями.
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

// Установите свойство "LayoutFlow", чтобы задать ориентацию текстового содержимого этого текстового поля.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

Показывает, как изменить размер текстового поля, чтобы оно полностью вмещало его содержимое.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Применяем эти значения к обоим членам, чтобы подогнать родительскую форму
// плотно обхватывает текстовое содержимое, игнорируя заданные нами размеры.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
