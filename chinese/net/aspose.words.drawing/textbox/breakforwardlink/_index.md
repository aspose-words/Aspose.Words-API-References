---
title: TextBox.BreakForwardLink
linktitle: BreakForwardLink
articleTitle: BreakForwardLink
second_title: Aspose.Words for .NET
description: 探索 TextBox BreakForwardLink 方法，无缝断开文本框之间的链接，提升用户体验和表单导航。立即优化您的 UI！
type: docs
weight: 130
url: /zh/net/aspose.words.drawing/textbox/breakforwardlink/
---
## TextBox.BreakForwardLink method

断开到下一个的链接[`TextBox`](../).

```csharp
public void BreakForwardLink()
```

## 评论

`BreakForwardLink`不会破坏当前形状序列中的所有其他链接。 例如：1-2-3-4 序列和`BreakForwardLink`在第二个文本框中将创建 两个序列 1-2、3-4。

## 例子

显示如何链接文本框。

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

// 在一些文本框之间创建链接。
if (textBox1.IsValidLinkTarget(textBox2))
    textBox1.Next = textBox2;

if (textBox2.IsValidLinkTarget(textBox3))
    textBox2.Next = textBox3;

// 只有空文本框才可能有链接。
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

    // 断开 textBox2 和 textBox3 之间的前向链接，然后验证它们不再链接。
    textBox3.Previous.BreakForwardLink();
    Assert.IsTrue(textBox2.Next == null);
    Assert.IsTrue(textBox3.Previous == null);
}

doc.Save(ArtifactsDir + "Shape.CreateLinkBetweenTextBoxes.docx");
```

### 也可以看看

* class [TextBox](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
