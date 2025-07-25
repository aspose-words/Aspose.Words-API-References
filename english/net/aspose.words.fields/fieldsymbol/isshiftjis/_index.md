---
title: FieldSymbol.IsShiftJis
linktitle: IsShiftJis
articleTitle: IsShiftJis
second_title: Aspose.Words for .NET
description: Discover the FieldSymbol IsShiftJis property—easily manage SHIFTJIS character codes for enhanced data handling and seamless character interpretation.
type: docs
weight: 70
url: /net/aspose.words.fields/fieldsymbol/isshiftjis/
---
## FieldSymbol.IsShiftJis property

Gets or sets whether the character code is interpreted as the value of a SHIFT-JIS character.

```csharp
public bool IsShiftJis { get; set; }
```

## Examples

Shows how to use the SYMBOL field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are three ways to use a SYMBOL field to display a single character.
// 1 -  Add a SYMBOL field which displays the © (Copyright) symbol, specified by an ANSI character code:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// The ANSI character code "U+00A9", or "169" in integer form, is reserved for the copyright symbol.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.That(field.GetFieldCode(), Is.EqualTo(" SYMBOL  169 \\a"));

builder.Writeln(" Line 1");

// 2 -  Add a SYMBOL field which displays the ∞ (Infinity) symbol, and modify its appearance:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// In Unicode, the infinity symbol occupies the "221E" code.
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Change the font of our symbol after using the Windows Character Map
// to ensure that the font can represent that symbol.
field.FontName = "Calibri";
field.FontSize = "24";

// We can set this flag for tall symbols to make them not push down the rest of the text on their line.
field.DontAffectsLineSpacing = true;

Assert.That(field.GetFieldCode(), Is.EqualTo(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h"));

builder.Writeln("Line 2");

// 3 -  Add a SYMBOL field which displays the あ character,
// with a font that supports Shift-JIS (Windows-932) codepage:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);
field.FontName = "MS Gothic";
field.CharacterCode = 0x82A0.ToString();
field.IsShiftJis = true;

Assert.That(field.GetFieldCode(), Is.EqualTo(" SYMBOL  33440 \\f \"MS Gothic\" \\j"));

builder.Write("Line 3");

doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### See Also

* class [FieldSymbol](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
