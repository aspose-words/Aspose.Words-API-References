---
title: LoadOptions.UpdateDirtyFields
linktitle: UpdateDirtyFields
articleTitle: UpdateDirtyFields
second_title: Aspose.Words for .NET
description: 了解 LoadOptions UpdateDirtyFields 属性如何通过选择性地更新标记为脏的字段来增强数据完整性，以获得最佳性能。
type: docs
weight: 160
url: /zh/net/aspose.words.loading/loadoptions/updatedirtyfields/
---
## LoadOptions.UpdateDirtyFields property

指定是否使用`肮脏的`属性.

```csharp
public bool UpdateDirtyFields { get; set; }
```

## 例子

展示如何使用特殊属性来更新字段结果。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 赋予文档内置的“Author”属性值，然后用字段显示它。
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// 更新属性。该字段仍显示旧值。
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// 由于该字段的值已过时，我们可以将其标记为“脏”。
// 此值将保持过时，直到我们使用 Field.Update() 方法手动更新该字段。
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // 如果我们保存而不调用更新方法，
    // 该字段将继续在输出文档中显示过时的值。
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

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
