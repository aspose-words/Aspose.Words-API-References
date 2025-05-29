---
title: FieldSymbol.CharacterCode
linktitle: CharacterCode
articleTitle: CharacterCode
second_title: Aspose.Words for .NET
description: 发现 FieldSymbol CharacterCode 属性，轻松检索或设置十进制或十六进制的字符代码值，实现无缝数据管理。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldsymbol/charactercode/
---
## FieldSymbol.CharacterCode property

获取或设置字符的代码点值（十进制或十六进制）。

```csharp
public string CharacterCode { get; set; }
```

## 例子

展示如何使用 SYMBOL 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是使用 SYMBOL 字段显示单个字符的三种方法。
// 1 - 添加一个 SYMBOL 字段，显示 ©（版权）符号，由 ANSI 字符代码指定：
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// ANSI 字符代码“U+00A9”，即整数形式的“169”，保留用于版权符号。
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - 添加一个显示 ∞（无穷大）符号的 SYMBOL 字段，并修改其外观：
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// 在 Unicode 中，无穷大符号占据“221E”代码。
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// 使用 Windows 字符映射表后更改符号的字体
// 以确保字体可以表示该符号。
field.FontName = "Calibri";
field.FontSize = "24";

// 我们可以为高符号设置此标志，以使它们不会将行上的其余文本向下推。
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - 添加一个显示 あ 字符的 SYMBOL 字段，
// 使用支持 Shift-JIS（Windows-932）代码页的字体：
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
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
