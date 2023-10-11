---
title: FieldSymbol.DontAffectsLineSpacing
second_title: Aspose.Words for .NET API 参考
description: FieldSymbol 财产. 获取或设置字段检索的字符是否影响段落的行距
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldsymbol/dontaffectslinespacing/
---
## FieldSymbol.DontAffectsLineSpacing property

获取或设置字段检索的字符是否影响段落的行距。

```csharp
public bool DontAffectsLineSpacing { get; set; }
```

### 例子

显示如何使用 SYMBOL 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是使用 SYMBOL 字段显示单个字符的三种方法。
// 1 - 添加一个 SYMBOL 字段，用于显示由 ANSI 字符代码指定的 ©（版权）符号：
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// ANSI 字符代码“U+00A9”，或整数形式的“169”，是为版权符号保留的。
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - 添加一个显示 Infinity 符号的 SYMBOL 字段，并修改其外观：
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// 在Unicode中，无穷大符号占据“221E”代码。
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// 使用 Windows 字符映射表后更改符号的字体
// 确保字体可以代表该符号。
field.FontName = "Calibri";
field.FontSize = "24";

// 我们可以为高符号设置此标志，以使它们不会向下推其行上的其余文本。
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

* class [FieldSymbol](../)
* 命名空间 [Aspose.Words.Fields](../../fieldsymbol/)
* 部件 [Aspose.Words](../../../)


