---
title: "Aspose::Words::Fields::FieldSymbol::get_IsUnicode-Methode"
linktitle: "get_IsUnicode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldSymbol::get_IsUnicode-Methode. Liest oder setzt, ob der Zeichencode als Wert eines Unicode‑Zeichens in C++ interpretiert wird."
type: docs
weight: 8000
url: /de/cpp/aspose.words.fields/fieldsymbol/get_isunicode/
---
## FieldSymbol::get_IsUnicode method


Ermittelt oder legt fest, ob der Zeichencode als Wert eines Unicode-Zeichens interpretiert wird.

```cpp
bool Aspose::Words::Fields::FieldSymbol::get_IsUnicode()
```


## Beispiele



Zeigt, wie das SYMBOL-Feld verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Im Folgenden sind drei Möglichkeiten aufgeführt, ein SYMBOL-Feld zu verwenden, um ein einzelnes Zeichen anzuzeigen.
// 1 -  Fügen Sie ein SYMBOL-Feld hinzu, das das © (Copyright)-Symbol anzeigt, angegeben durch einen ANSI-Zeichencode:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// Der ANSI-Zeichencode "U+00A9" bzw. "169" in Ganzzahlform ist für das Copyright-Symbol reserviert.
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 -  Fügen Sie ein SYMBOL-Feld hinzu, das das ∞ (Unendlichkeit)-Symbol anzeigt, und ändern Sie dessen Darstellung:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// Im Unicode belegt das Unendlichkeitssymbol den Code "221E".
field->set_CharacterCode(System::Convert::ToString(0x221E));
field->set_IsUnicode(true);

// Ändern Sie die Schriftart unseres Symbols, nachdem Sie die Windows-Zeichentabelle verwendet haben
// um sicherzustellen, dass die Schriftart dieses Symbol darstellen kann.
field->set_FontName(u"Calibri");
field->set_FontSize(u"24");

// Wir können dieses Flag für hohe Symbole setzen, damit sie den restlichen Text in ihrer Zeile nicht nach unten schieben.
field->set_DontAffectsLineSpacing(true);

ASSERT_EQ(u" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field->GetFieldCode());

builder->Writeln(u"Line 2");

// 3 -  Fügen Sie ein SYMBOL-Feld hinzu, das das Zeichen あ anzeigt,
// mit einer Schriftart, die die Shift-JIS (Windows-932)-Codepage unterstützt:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Siehe auch

* Class [FieldSymbol](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
