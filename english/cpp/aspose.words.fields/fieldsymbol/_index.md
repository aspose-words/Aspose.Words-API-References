---
title: Aspose::Words::Fields::FieldSymbol class
linktitle: FieldSymbol
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldSymbol class. Implements a SYMBOL field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 98000
url: /cpp/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class


Implements a SYMBOL field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldSymbol : public Aspose::Words::Fields::Field,
                    public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_CharacterCode](./get_charactercode/)() | Gets or sets the character's code point value in decimal or hexadecimal. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_DontAffectsLineSpacing](./get_dontaffectslinespacing/)() | Gets or sets whether the character retrieved by the field affects the line spacing of the paragraph. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_FontName](./get_fontname/)() | Gets or sets the name of the font of the character retrieved by the field. |
| [get_FontSize](./get_fontsize/)() | Gets or sets the size in points of the font of the character retrieved by the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsAnsi](./get_isansi/)() | Gets or sets whether the character code is interpreted as the value of an ANSI character. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_IsShiftJis](./get_isshiftjis/)() | Gets or sets whether the character code is interpreted as the value of a SHIFT-JIS character. |
| [get_IsUnicode](./get_isunicode/)() | Gets or sets whether the character code is interpreted as the value of a Unicode character. |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_CharacterCode](./set_charactercode/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldSymbol::get_CharacterCode](./get_charactercode/). |
| [set_DontAffectsLineSpacing](./set_dontaffectslinespacing/)(bool) | Setter for [Aspose::Words::Fields::FieldSymbol::get_DontAffectsLineSpacing](./get_dontaffectslinespacing/). |
| [set_FontName](./set_fontname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldSymbol::get_FontName](./get_fontname/). |
| [set_FontSize](./set_fontsize/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldSymbol::get_FontSize](./get_fontsize/). |
| [set_IsAnsi](./set_isansi/)(bool) | Setter for [Aspose::Words::Fields::FieldSymbol::get_IsAnsi](./get_isansi/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsShiftJis](./set_isshiftjis/)(bool) | Setter for [Aspose::Words::Fields::FieldSymbol::get_IsShiftJis](./get_isshiftjis/). |
| [set_IsUnicode](./set_isunicode/)(bool) | Setter for [Aspose::Words::Fields::FieldSymbol::get_IsUnicode](./get_isunicode/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to use the SYMBOL field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Below are three ways to use a SYMBOL field to display a single character.
// 1 -  Add a SYMBOL field which displays the © (Copyright) symbol, specified by an ANSI character code:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// The ANSI character code "U+00A9", or "169" in integer form, is reserved for the copyright symbol.
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 -  Add a SYMBOL field which displays the ∞ (Infinity) symbol, and modify its appearance:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

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
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
