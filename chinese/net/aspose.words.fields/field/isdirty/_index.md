---
title: Field.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: 用于 .NET 的 Aspose.Words
description: Field IsDirty 财产. 获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确陈旧 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.fields/field/isdirty/
---
## Field.IsDirty property

获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。

```csharp
public bool IsDirty { get; set; }
```

## 例子

展示如何使用特殊属性来更新字段结果。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 给出文档的内置“Author”属性值，然后用字段显示它。
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// 更新属性。该字段仍显示旧值。
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// 由于该字段的值已过时，我们可以将其标记为“脏”。
// 在我们使用 Field.Update() 方法手动更新字段之前，该值将保持过时状态。
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // 如果我们保存而不调用更新方法，
    // 该字段将在输出文档中继续显示过期值。
    doc.Save(docStream, SaveFormat.Docx);

    // LoadOptions 对象有一个更新所有字段的选项
    // 加载文档时标记为“脏”。
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // 像这样更新脏字段会自动将其“IsDirty”标志设置为 false。
    if (updateDirtyFields)
    {
        Assert.AreEqual("John & Jane Doe", field.Result);
        Assert.False(field.IsDirty);
    }
    else
    {
        Assert.AreEqual("John Doe", field.Result);
        Assert.True(field.IsDirty);
    }
}
```

### 也可以看看

* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
