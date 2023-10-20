---
title: FieldAutoNumLgl.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: 用于 .NET 的 Aspose.Words
description: FieldAutoNumLgl SeparatorCharacter 财产. 获取或设置要使用的分隔符 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldautonumlgl/separatorcharacter/
---
## FieldAutoNumLgl.SeparatorCharacter property

获取或设置要使用的分隔符。

```csharp
public string SeparatorCharacter { get; set; }
```

## 例子

显示如何使用 AUTONUMLGL 字段组织文档。

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // AUTONUMLGL 字段显示一个数字，该数字在其当前标题级别内的每个 AUTONUMLGL 字段处递增。
    // 这些字段为每个标题级别维护一个单独的计数，
     // 并且每个字段还显示其下方所有标题级别的 AUTONUMLGL 字段计数。
    // 更改任何标题级别的计数会将高于该级别的所有级别的计数重置为 1。
    // 这允许我们以大纲列表的形式组织我们的文档。
    // 这是标题级别为 1 的第一个 AUTONUMLGL 字段，显示“1”。在文档中。
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // 这是标题级别为 1 的第二个 AUTONUMLGL 字段，因此它将显示“2.”。
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // 这是标题级别为 2 的第一个 AUTONUMLGL 字段，
    // 其下方标题级别的 AUTONUMLGL 计数为“2”，因此将显示“2.1.”。
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // 这是标题级别为 3 的第一个 AUTONUMLGL 字段。
    // 与上面字段的工作方式相同，它将显示“2.1.1.”。
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // 该字段的标题级别为 2，其各自的 AUTONUMLGL 计数为 2，因此该字段将显示“2.2.”。
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // 增加标题级别以下的 AUTONUMLGL 计数
    // 已重置此级别的计数，以便此字段显示“2.2.1.”。
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal))
    {
        // 分隔符，出现在字段结果中紧跟数字之后，
        // 默认情况下是句号。如果我们将此属性保留为空，
        // 我们最后一个 AUTONUMLGL 字段将显示“2.2.1”。在文档中。
        Assert.IsNull(field.SeparatorCharacter);

        // 设置自定义分隔符并删除尾随句点
        // 将从“2.2.1”更改该字段的外观。到“2:2:1”。
        // 我们将把它应用于我们创建的所有字段。
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");

/// <summary>
/// 使用文档构建器插入由 AUTONUMLGL 字段编号的子句。
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // 此文本将属于其上方的自动编号合法字段。
    // 当我们单击 Microsoft Word 中相应 AUTONUMLGL 字段旁边的箭头时，它将折叠。
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### 也可以看看

* class [FieldAutoNumLgl](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
