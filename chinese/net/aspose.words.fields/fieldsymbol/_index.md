---
title: FieldSymbol Class
linktitle: FieldSymbol
articleTitle: FieldSymbol
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.FieldSymbol 班级. 实现一个 SYMBOL 字段 在 C#.
type: docs
weight: 2460
url: /zh/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

实现一个 SYMBOL 字段。

```csharp
public class FieldSymbol : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldSymbol](fieldsymbol/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode/) { get; set; } | 获取或设置十进制或十六进制字符的代码点值。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing/) { get; set; } | 获取或设置字段检索到的字符是否影响段落的行距 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段end的节点。 |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname/) { get; set; } | 获取或设置字段检索到的字符的字体名称。 |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize/) { get; set; } | 获取或设置字段检索到的字符的字体大小。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 得到一个[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi/) { get; set; } | 获取或设置字符代码是否被解释为 ANSI 字符的值。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis/) { get; set; } | 获取或设置字符代码是否被解释为 SHIFT-JIS 字符的值。 |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode/) { get; set; } | 获取或设置字符代码是否被解释为 Unicode 字符的值。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（或字段结束，如果没有分隔符）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回**无效的**. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果该字段已被更新，则抛出。 |

## 评论

检索其代码点值以十进制或十六进制指定的字符。

## 例子

显示如何使用 SYMBOL 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是使用 SYMBOL 字段显示单个字符的三种方法。
// 1 - 添加一个 SYMBOL 字段，显示 ©（版权）符号，由 ANSI 字符代码指定：
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// ANSI 字符代码“U+00A9”，或整数形式的“169”，为版权符号保留。
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - 添加一个显示 ∞（无穷大）符号的 SYMBOL 字段，并修改其外观：
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// 在Unicode中，无穷大符号占据“221E”码。
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// 使用 Windows 字符映射后更改我们符号的字体
// 确保字体可以代表该符号。
field.FontName = "Calibri";
field.FontSize = "24";

// 我们可以为高大的符号设置此标志，以使它们不会压低行上的其余文本。
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - 添加一个显示 あ 字符的 SYMBOL 字段，
// 使用支持 Shift-JIS (Windows-932) 代码页的字体：
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);
field.FontName = "MS Gothic";
field.CharacterCode = 0x82A0.ToString();
field.IsShiftJis = true;

Assert.AreEqual(" SYMBOL  33440 \\f \"MS Gothic\" \\j", field.GetFieldCode());

builder.Write("Line 3");

doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
