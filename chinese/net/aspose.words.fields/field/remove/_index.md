---
title: Field.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: 使用“字段移除”方法轻松从文档中删除字段。获取精确的节点返回值并无缝处理空字段。优化您的工作流程！
type: docs
weight: 120
url: /zh/net/aspose.words.fields/field/remove/
---
## Field.Remove method

从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`.

```csharp
public Node Remove()
```

## 例子

展示如何从字段集合中删除字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// 以下是从字段集合中删除字段的四种方法。
// 1 - 获取要删除的字段：
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - 获取要删除的字段的集合，并将其传递给其删除方法：
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - 从集合中移除索引处的字段：
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - 一次性从集合中删除所有字段：
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

展示如何处理 PRIVATE 字段。

```csharp
public void FieldPrivate()
{
    // 打开我们已转换为 .docx 格式的 Corel WordPerfect 文档。
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // 我们加载的 WordPerfect 5.x/6.x 文档可能包含 PRIVATE 字段。
    // Microsoft Word 在加载/保存操作期间保留 PRIVATE 字段，
    // 但没有为它们提供任何功能。
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // 我们还可以使用文档构建器插入 PRIVATE 字段。
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // 这些字段不是保护敏感信息的可行方法。
    // 除非与旧版本的 WordPerfect 的向后兼容性至关重要，
    // 我们可以安全地删除这些字段。我们可以使用 DocumentVisiitor 实现来实现这一点。
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// 删除所有遇到的 PRIVATE 字段。
/// </summary>
public class FieldPrivateRemover : DocumentVisitor
{
    public FieldPrivateRemover()
    {
        mFieldsRemovedCount = 0;
    }

    public int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    /// <summary>
    /// 当在文档中遇到 FieldEnd 节点时调用。
    /// 如果节点属于 PRIVATE 字段，则删除整个字段。
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.FieldType == FieldType.FieldPrivate)
        {
            fieldEnd.GetField().Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction.Continue;
    }

    private int mFieldsRemovedCount;
}
```

### 也可以看看

* class [Node](../../../aspose.words/node/)
* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
