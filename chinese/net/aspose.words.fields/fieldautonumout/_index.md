---
title: FieldAutoNumOut Class
linktitle: FieldAutoNumOut
articleTitle: FieldAutoNumOut
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldAutoNumOut 类，实现无缝 AUTONUMOUT 字段实现，增强文档自动化和效率。
type: docs
weight: 2010
url: /zh/net/aspose.words.fields/fieldautonumout/
---
## FieldAutoNumOut class

实现 AUTONUMOUT 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldAutoNumOut : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldAutoNumOut](fieldautonumout/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式进行类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以是`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果字段已在更新，则抛出异常。 |

## 评论

以大纲格式插入自动编号。

## 例子

展示如何使用 AUTONUMOUT 字段对段落进行编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTONUMOUT 字段显示一个在每个 AUTONUMOUT 字段处递增的数字。
// 与 AUTONUM 字段不同，AUTONUMOUT 字段使用大纲编号方案，
// 我们可以在 Microsoft Word 中通过格式 -> 项目符号和编号 ->“大纲编号”进行定义。
// 这使我们能够像编号列表一样自动对项目进行编号。
// LISTNUM 字段是 AUTONUMOUT 字段的较新替代方案。
// 该字段将显示“1。”。
builder.InsertField(FieldType.FieldAutoNumOutline, true);
builder.Writeln("\tParagraph 1.");

// 此字段将显示“2。”。
builder.InsertField(FieldType.FieldAutoNumOutline, true);
builder.Writeln("\tParagraph 2.");

foreach (FieldAutoNumOut field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumOutline).ToList())
    Assert.AreEqual(" AUTONUMOUT ", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUMOUT.docx");
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
