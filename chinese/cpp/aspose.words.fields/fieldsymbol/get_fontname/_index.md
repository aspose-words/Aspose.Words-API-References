---
title: "Aspose::Words::Fields::FieldSymbol::get_FontName 方法"
linktitle: "get_FontName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldSymbol::get_FontName 方法。获取或设置字段检索的字符的字体名称（在 C++ 中）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.fields/fieldsymbol/get_fontname/
---
## FieldSymbol::get_FontName method


获取或设置字段检索的字符的字体名称。

```cpp
System::String Aspose::Words::Fields::FieldSymbol::get_FontName()
```


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

* Class [FieldSymbol](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
