---
title: get_CharacterCode
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the character's code point value in decimal or hexadecimal.
type: docs
weight: 14
url: /cpp/aspose.words.fields/fieldsymbol/get_charactercode/
---
## FieldSymbol::get_CharacterCode method


Gets or sets the character's code point value in decimal or hexadecimal.

```cpp
System::String Aspose::Words::Fields::FieldSymbol::get_CharacterCode()
```


## Examples



Shows how to use the SYMBOL field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are three ways to use a SYMBOL field to display a single character.
// 1 -  Add a SYMBOL field which displays the © (Copyright) symbol, specified by an ANSI character code:
auto field = System::DynamicCast<FieldSymbol>(builder->InsertField(FieldType::FieldSymbol, true));

// The ANSI character code "U+00A9", or "169" in integer form, is reserved for the copyright symbol.
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 -  Add a SYMBOL field which displays the ∞ (Infinity) symbol, and modify its appearance:
field = System::DynamicCast<FieldSymbol>(builder->InsertField(FieldType::FieldSymbol, true));

// In Unicode, the infinity symbol occupies the "221E" code.
field->set_CharacterCode(System::Convert::ToString(0x221E));
field->set_IsUnicode(true);

// Change the font of our symbol after using the Windows Character Map
// to ensure that the font can represent that symbol.
field->set_FontName(u"Calibri");
field->set_FontSize(u"24");

// We can set this flag for tall symbols to make them not push down the rest of the text on their line.
field->set_DontAffectsLineSpacing(true);

ASSERT_EQ(u" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field->GetFieldCode());

builder->Writeln(u"Line 2");

// 3 -  Add a SYMBOL field which displays the あ character,
// with a font that supports Shift-JIS (Windows-932) codepage:
field = System::DynamicCast<FieldSymbol>(builder->InsertField(FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(ArtifactsDir + u"Field.SYMBOL.docx");
```

## See Also

* Class [FieldSymbol](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
