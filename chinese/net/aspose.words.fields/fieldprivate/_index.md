---
title: FieldPrivate
second_title: Aspose.Words for .NET API 参考
description: 实现 PRIVATE 字段
type: docs
weight: 2150
url: /zh/net/aspose.words.fields/fieldprivate/
---
## FieldPrivate class

实现 PRIVATE 字段。

```csharp
public class FieldPrivate : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldPrivate](fieldprivate)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end) { get; } | 获取代表字段end的节点。 |
| [Format](../../aspose.words.fields/field/format) { get; } | 得到一个[`FieldFormat`](../fieldformat)提供对字段格式的类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | 获取或设置字段的LCID。 |
| [Result](../../aspose.words.fields/field/result) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [Start](../../aspose.words.fields/field/start) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | 返回字段开始和字段分隔符之间的文本（或字段结束，如果没有分隔符）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove)() | 从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回 **无效的**. |
| [Unlink](../../aspose.words.fields/field/unlink)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update)() | 执行字段更新。如果该字段已被更新，则抛出。 |
| [Update](../../aspose.words.fields/field/update)(bool) | 执行字段更新。如果该字段已被更新，则抛出。 |

### 评论

提供私有存储区域。此字段用于存储从 other 文件格式转换的文档的数据。

### 例子

显示如何处理 PRIVATE 字段。

```csharp
{
    // 打开已转换为 .docx 格式的 Corel WordPerfect 文档。
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // WordPerfect 5.x/6.x 文档，例如我们加载的文档，可能包含 PRIVATE 字段。
    // Microsoft Word 在加载/保存操作期间保留 PRIVATE 字段，
    // 但不为它们提供任何功能。
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // 我们还可以使用文档构建器插入 PRIVATE 字段。
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // 这些字段不是保护敏感信息的可行方法。
    // 除非向后兼容旧版本的 WordPerfect 是必不可少的，
    // 我们可以安全地删除这些字段。我们可以使用 DocumentVisiitor 实现来做到这一点。
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
    /// 在文档中遇到 FieldEnd 节点时调用。
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

* class [Field](../field)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->