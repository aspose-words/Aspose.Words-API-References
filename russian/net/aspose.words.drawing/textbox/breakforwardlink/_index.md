---
title: TextBox.BreakForwardLink
linktitle: BreakForwardLink
articleTitle: BreakForwardLink
second_title: Aspose.Words для .NET
description: Откройте для себя метод TextBox BreakForwardLink, чтобы легко отсоединить ваши TextBox, улучшая пользовательский опыт и навигацию по формам. Оптимизируйте свой пользовательский интерфейс сегодня!
type: docs
weight: 130
url: /ru/net/aspose.words.drawing/textbox/breakforwardlink/
---
## TextBox.BreakForwardLink method

Разрывает ссылку на следующий[`TextBox`](../) .

```csharp
public void BreakForwardLink()
```

## Примечания

`BreakForwardLink` не нарушает все остальные связи в текущей последовательности фигур. Например: последовательность 1-2-3-4 и`BreakForwardLink` во 2-м текстовом поле создаст две последовательности 1-2, 3-4.

## Примеры

Показывает, как связывать текстовые поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape1 = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox1 = textBoxShape1.TextBox;
builder.Writeln();

Shape textBoxShape2 = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox2 = textBoxShape2.TextBox;
builder.Writeln();

Shape textBoxShape3 = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox3 = textBoxShape3.TextBox;
builder.Writeln();

Shape textBoxShape4 = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox4 = textBoxShape4.TextBox;

// Создайте связи между некоторыми текстовыми полями.
if (textBox1.IsValidLinkTarget(textBox2))
    textBox1.Next = textBox2;

if (textBox2.IsValidLinkTarget(textBox3))
    textBox2.Next = textBox3;

// Ссылку можно разместить только в пустом текстовом поле.
Assert.True(textBox3.IsValidLinkTarget(textBox4));

builder.MoveTo(textBoxShape4.LastParagraph);
builder.Write("Hello world!");

Assert.False(textBox3.IsValidLinkTarget(textBox4));

if (textBox1.Next != null && textBox1.Previous == null)
    Console.WriteLine("This TextBox is the head of the sequence");

if (textBox2.Next != null && textBox2.Previous != null)
    Console.WriteLine("This TextBox is the middle of the sequence");

if (textBox3.Next == null && textBox3.Previous != null)
{
    Console.WriteLine("This TextBox is the tail of the sequence");

    // Разорвать прямую ссылку между textBox2 и textBox3, а затем убедиться, что они больше не связаны.
    textBox3.Previous.BreakForwardLink();
    Assert.IsTrue(textBox2.Next == null);
    Assert.IsTrue(textBox3.Previous == null);
}

doc.Save(ArtifactsDir + "Shape.CreateLinkBetweenTextBoxes.docx");
```

### Смотрите также

* class [TextBox](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
