---
title: FieldAutoNumLgl Class
linktitle: FieldAutoNumLgl
articleTitle: FieldAutoNumLgl
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.FieldAutoNumLgl 班级. 实现 AUTONUMLGL 字段 在 C#.
type: docs
weight: 1590
url: /zh/net/aspose.words.fields/fieldautonumlgl/
---
## FieldAutoNumLgl class

实现 AUTONUMLGL 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldAutoNumLgl : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldAutoNumLgl](fieldautonumlgl/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示的字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取表示字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [RemoveTrailingPeriod](../../aspose.words.fields/fieldautonumlgl/removetrailingperiod/) { get; set; } | 获取或设置是否显示不带尾随句点的数字。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结束之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可`无效的`. |
| [SeparatorCharacter](../../aspose.words.fields/fieldautonumlgl/separatorcharacter/) { get; set; } | 获取或设置要使用的分隔符。 |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除该字段。返回字段后面的节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果该字段已被更新，则抛出异常。 |

## 评论

以合法格式插入自动编号。

## 例子

演示如何使用 AUTONUMLGL 字段组织文档。

```csharp
public void FieldAutoNumLgl()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // AUTONUMLGL 字段显示一个数字，该数字在当前标题级别内的每个 AUTONUMLGL 字段处递增。
    // 这些字段为每个标题级别维护单独的计数，
     // 并且每个字段还显示低于其自身的所有标题级别的 AUTONUMLGL 字段计数。
    // 更改任何标题级别的计数都会将该级别之上的所有级别的计数重置为 1。
    // 这允许我们以大纲列表的形式组织文档。
    // 这是标题级别为 1 的第一个 AUTONUMLGL 字段，显示“1”。在文件中。
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // 这是标题级别为 1 的第二个 AUTONUMLGL 字段，因此它将显示“2.”。
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // 这是标题级别为 2 的第一个 AUTONUMLGL 字段，
    // 并且其下方标题级别的 AUTONUMLGL 计数为“2”，因此它将显示“2.1.”。
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // 这是标题级别为 3 的第一个 AUTONUMLGL 字段。
    // 与上面字段的操作方式相同，它将显示“2.1.1.”。
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // 该字段的标题级别为 2，其相应的 AUTONUMLGL 计数为 2，因此该字段将显示“2.2.”。
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // 增加低于此级别的标题级别的 AUTONUMLGL 计数
    // 已重置该级别的计数，以便该字段将显示“2.2.1.”。
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal))
    {
        // 分隔符，出现在字段结果中紧跟数字之后，
        // 默认是句号。如果我们将此属性保留为空，
        // 我们的最后一个 AUTONUMLGL 字段将显示“2.2.1”。在文件中。
        Assert.IsNull(field.SeparatorCharacter);

        // 设置自定义分隔符并删除尾随句点
        // 将从“2.2.1”更改该字段的外观。到“2:2:1”。
        // 我们将把它应用到我们创建的所有字段。
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// 使用文档生成器插入由 AUTONUMLGL 字段编号的子句。
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // 该文本将属于其上方的 auto num 合法字段。
    // 当我们单击 Microsoft Word 中相应 AUTONUMLGL 字段旁边的箭头时，它将折叠。
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
