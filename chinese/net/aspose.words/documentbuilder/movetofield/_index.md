---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder MoveToField 方法. 将光标移动到文档中的字段 在 C#.
type: docs
weight: 530
url: /zh/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

将光标移动到文档中的字段。

```csharp
public void MoveToField(Field field, bool isAfter)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field | Field | 将光标移动到的字段。 |
| isAfter | Boolean | 什么时候`真的` , 将光标移动到字段末尾之后。 时`错误的`，将光标移动到字段开始之前。 |

## 例子

演示如何将文档生成器的节点插入点光标移动到特定字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 DocumentBuilder 插入一个字段并在其后添加一段文本。
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// 构建器的光标当前位于文档末尾。
Assert.Null(builder.CurrentNode);

// 将光标移动到字段，同时指定是将光标放置在字段之前还是之后。
builder.MoveToField(field, moveCursorToAfterTheField);

// 请注意，在这两种情况下，光标都位于字段之外。
// 这意味着我们不能像这样使用构建器编辑字段。
// 要编辑字段，我们可以在字段的 FieldStart 上使用构建器的 MoveTo 方法
// 或 FieldSeparator 节点将光标放置在其中。
if (moveCursorToAfterTheField)
{
    Assert.Null(builder.CurrentNode);
    builder.Write(" Text immediately after the field.");

    Assert.AreEqual("\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", 
        doc.GetText().Trim());
}
else
{
    Assert.AreEqual(field.Start, builder.CurrentNode);
    builder.Write("Text immediately before the field. ");

    Assert.AreEqual("Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", 
        doc.GetText().Trim());
}
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
