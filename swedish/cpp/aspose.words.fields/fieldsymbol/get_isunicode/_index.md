---
title: "Aspose::Words::Fields::FieldSymbol::get_IsUnicode metod"
linktitle: "get_IsUnicode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldSymbol::get_IsUnicode method. Hämtar eller anger om teckenkoden tolkas som värdet för ett Unicode-tecken i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.fields/fieldsymbol/get_isunicode/
---
## FieldSymbol::get_IsUnicode method


Hämtar eller anger om teckenkoden tolkas som värdet för ett Unicode-tecken.

```cpp
bool Aspose::Words::Fields::FieldSymbol::get_IsUnicode()
```


## Exempel



Visar hur man använder SYMBOL-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan följer tre sätt att använda ett SYMBOL-fält för att visa ett enda tecken.
// 1 -  Lägg till ett SYMBOL-fält som visar © (Copyright)-symbolen, specificerad med en ANSI-teckenkod:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// ANSI-teckenkoden "U+00A9", eller "169" i heltalsform, är reserverad för copyright‑symbolen.
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 -  Lägg till ett SYMBOL-fält som visar ∞ (Oändlighet)-symbolen och ändra dess utseende:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// I Unicode upptar oändlighetssymbolen koden "221E".
field->set_CharacterCode(System::Convert::ToString(0x221E));
field->set_IsUnicode(true);

// Ändra teckensnittet för vår symbol efter att ha använt Windows teckenkarta
// för att säkerställa att teckensnittet kan representera den symbolen.
field->set_FontName(u"Calibri");
field->set_FontSize(u"24");

// Vi kan sätta den här flaggan för höga symboler så att de inte skjuter ner resten av texten på deras rad.
field->set_DontAffectsLineSpacing(true);

ASSERT_EQ(u" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field->GetFieldCode());

builder->Writeln(u"Line 2");

// 3 -  Lägg till ett SYMBOL-fält som visar tecknet あ,
// med ett teckensnitt som stöder Shift-JIS (Windows-932)-teckensätt:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Se även

* Class [FieldSymbol](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
