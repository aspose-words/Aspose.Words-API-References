---
title: "Aspose::Words::Fields::FieldSymbol 类"
linktitle: "FieldSymbol"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldSymbol 类。实现了 SYMBOL 字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 98000
url: /zh/cpp/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class


实现 SYMBOL 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldSymbol : public Aspose::Words::Fields::Field,
                    public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_CharacterCode](./get_charactercode/)() | 获取或设置字符的代码点值（十进制或十六进制）。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_DontAffectsLineSpacing](./get_dontaffectslinespacing/)() | 获取或设置字段检索的字符是否影响段落的行距。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_FontName](./get_fontname/)() | 获取或设置字段检索的字符的字体名称。 |
| [get_FontSize](./get_fontsize/)() | 获取或设置字段检索的字符的字体大小（磅）。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsAnsi](./get_isansi/)() | 获取或设置字符代码是否被解释为 ANSI 字符的值。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_IsShiftJis](./get_isshiftjis/)() | 获取或设置字符代码是否被解释为 SHIFT-JIS 字符的值。 |
| [get_IsUnicode](./get_isunicode/)() | 获取或设置字符码是否被解释为 Unicode 字符的值。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_CharacterCode](./set_charactercode/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldSymbol::get_CharacterCode](./get_charactercode/)。 |
| [set_DontAffectsLineSpacing](./set_dontaffectslinespacing/)(bool) | 用于设置 [Aspose::Words::Fields::FieldSymbol::get_DontAffectsLineSpacing](./get_dontaffectslinespacing/)。 |
| [set_FontName](./set_fontname/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldSymbol::get_FontName](./get_fontname/)。 |
| [set_FontSize](./set_fontsize/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldSymbol::get_FontSize](./get_fontsize/)。 |
| [set_IsAnsi](./set_isansi/)(bool) | 用于设置 [Aspose::Words::Fields::FieldSymbol::get_IsAnsi](./get_isansi/)。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_IsShiftJis](./set_isshiftjis/)(bool) | 用于设置 [Aspose::Words::Fields::FieldSymbol::get_IsShiftJis](./get_isshiftjis/)。 |
| [set_IsUnicode](./set_isunicode/)(bool) | 用于设置 [Aspose::Words::Fields::FieldSymbol::get_IsUnicode](./get_isunicode/)。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



展示如何使用 SYMBOL 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 以下是使用 SYMBOL 字段显示单个字符的三种方法。
// 1 - 添加一个显示 ©（版权）符号的 SYMBOL 字段，由 ANSI 字符码指定：
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// ANSI 字符码 "U+00A9"，或整数形式的 "169"，专用于版权符号。
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 - 添加一个显示 ∞（无限）符号的 SYMBOL 字段，并修改其外观：
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// 在 Unicode 中，无限符号的代码是 "221E"。
field->set_CharacterCode(System::Convert::ToString(0x221E));
field->set_IsUnicode(true);

// 在使用 Windows 字符映射表后更改我们符号的字体
// 以确保该字体能够表示该符号。
field->set_FontName(u"Calibri");
field->set_FontSize(u"24");

// 我们可以为高的符号设置此标志，使其不会把同一行其余文本向下推。
field->set_DontAffectsLineSpacing(true);

ASSERT_EQ(u" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field->GetFieldCode());

builder->Writeln(u"Line 2");

// 3 - 添加一个显示 あ 字符的 SYMBOL 字段，
// 使用支持 Shift-JIS（Windows-932）代码页的字体：
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
