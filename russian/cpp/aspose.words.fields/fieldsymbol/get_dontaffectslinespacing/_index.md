---
title: "Aspose::Words::Fields::FieldSymbol::get_DontAffectsLineSpacing метод"
linktitle: "get_DontAffectsLineSpacing"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldSymbol::get_DontAffectsLineSpacing метод. Получает или задает, влияет ли символ, полученный полем, на межстрочный интервал абзаца в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fields/fieldsymbol/get_dontaffectslinespacing/
---
## FieldSymbol::get_DontAffectsLineSpacing method


Получает или задает, влияет ли символ, полученный полем, на межстрочный интервал абзаца.

```cpp
bool Aspose::Words::Fields::FieldSymbol::get_DontAffectsLineSpacing()
```


## Примеры



Показывает, как использовать поле SYMBOL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены три способа использования поля SYMBOL для отображения одного символа.
// 1 -  Добавьте поле SYMBOL, которое отображает символ © (Copyright), указанный ANSI-кодом символа:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// ANSI-код символа "U+00A9" или "169" в целочисленном виде зарезервирован для символа копирайта.
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 -  Добавьте поле SYMBOL, которое отображает символ ∞ (Infinity), и измените его внешний вид:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// В Unicode символ бесконечности занимает код "221E".
field->set_CharacterCode(System::Convert::ToString(0x221E));
field->set_IsUnicode(true);

// Измените шрифт нашего символа после использования Windows Character Map
// чтобы убедиться, что шрифт может отобразить этот символ.
field->set_FontName(u"Calibri");
field->set_FontSize(u"24");

// Мы можем установить этот флаг для высоких символов, чтобы они не опускали остальной текст в своей строке.
field->set_DontAffectsLineSpacing(true);

ASSERT_EQ(u" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field->GetFieldCode());

builder->Writeln(u"Line 2");

// 3 -  Добавьте поле SYMBOL, которое отображает символ あ,
// со шрифтом, поддерживающим кодовую страницу Shift-JIS (Windows-932):
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## См. также

* Class [FieldSymbol](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
