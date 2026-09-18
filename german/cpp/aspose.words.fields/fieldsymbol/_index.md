---
title: "Aspose::Words::Fields::FieldSymbol Klasse"
linktitle: "FieldSymbol"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldSymbol Klasse. Implementiert ein SYMBOL-Feld. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 98000
url: /de/cpp/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class


Implementiert ein SYMBOL-Feld. Weitere Informationen finden Sie im [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldSymbol : public Aspose::Words::Fields::Field,
                    public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_CharacterCode](./get_charactercode/)() | Ermittelt oder legt den Codepunktwert des Zeichens in Dezimal- oder Hexadezimaldarstellung fest. |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_DontAffectsLineSpacing](./get_dontaffectslinespacing/)() | Ermittelt oder legt fest, ob das vom Feld abgerufene Zeichen den Zeilenabstand des Absatzes beeinflusst. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_FontName](./get_fontname/)() | Ermittelt oder legt den Namen der Schriftart des vom Feld abgerufenen Zeichens fest. |
| [get_FontSize](./get_fontsize/)() | Ermittelt oder legt die Größe in Punkten der Schriftart des vom Feld abgerufenen Zeichens fest. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_IsAnsi](./get_isansi/)() | Ermittelt oder legt fest, ob der Zeichencode als Wert eines ANSI-Zeichens interpretiert wird. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_IsShiftJis](./get_isshiftjis/)() | Ermittelt oder legt fest, ob der Zeichencode als Wert eines SHIFT-JIS-Zeichens interpretiert wird. |
| [get_IsUnicode](./get_isunicode/)() | Ermittelt oder legt fest, ob der Zeichencode als Wert eines Unicode-Zeichens interpretiert wird. |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_CharacterCode](./set_charactercode/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldSymbol::get_CharacterCode](./get_charactercode/). |
| [set_DontAffectsLineSpacing](./set_dontaffectslinespacing/)(bool) | Setter für [Aspose::Words::Fields::FieldSymbol::get_DontAffectsLineSpacing](./get_dontaffectslinespacing/). |
| [set_FontName](./set_fontname/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldSymbol::get_FontName](./get_fontname/). |
| [set_FontSize](./set_fontsize/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldSymbol::get_FontSize](./get_fontsize/). |
| [set_IsAnsi](./set_isansi/)(bool) | Setter für [Aspose::Words::Fields::FieldSymbol::get_IsAnsi](./get_isansi/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsShiftJis](./set_isshiftjis/)(bool) | Setter für [Aspose::Words::Fields::FieldSymbol::get_IsShiftJis](./get_isshiftjis/). |
| [set_IsUnicode](./set_isunicode/)(bool) | Setter für [Aspose::Words::Fields::FieldSymbol::get_IsUnicode](./get_isunicode/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
