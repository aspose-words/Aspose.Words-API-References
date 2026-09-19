---
title: "Aspose::Words::Fields::FieldSymbol::get_CharacterCode metodo"
linktitle: "get_CharacterCode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldSymbol::get_CharacterCode metodo. Ottiene o imposta il valore del punto di codice del carattere in decimale o esadecimale in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldsymbol/get_charactercode/
---
## FieldSymbol::get_CharacterCode method


Ottiene o imposta il valore del punto di codice del carattere in decimale o esadecimale.

```cpp
System::String Aspose::Words::Fields::FieldSymbol::get_CharacterCode()
```


## Esempi



Mostra come utilizzare il campo SYMBOL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati tre modi per utilizzare un campo SYMBOL per visualizzare un singolo carattere.
// 1 -  Aggiungi un campo SYMBOL che visualizza il simbolo © (Copyright), specificato da un codice di carattere ANSI:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// Il codice di carattere ANSI "U+00A9", o "169" in forma intera, è riservato per il simbolo di copyright.
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 -  Aggiungi un campo SYMBOL che visualizza il simbolo ∞ (Infinito), e modifica il suo aspetto:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// In Unicode, il simbolo dell'infinito occupa il codice "221E".
field->set_CharacterCode(System::Convert::ToString(0x221E));
field->set_IsUnicode(true);

// Modifica il carattere del nostro simbolo dopo aver usato la Mappa dei caratteri di Windows
// per garantire che il carattere possa rappresentare quel simbolo.
field->set_FontName(u"Calibri");
field->set_FontSize(u"24");

// Possiamo impostare questa opzione per i simboli alti in modo che non spingano verso il basso il resto del testo sulla loro riga.
field->set_DontAffectsLineSpacing(true);

ASSERT_EQ(u" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field->GetFieldCode());

builder->Writeln(u"Line 2");

// 3 -  Aggiungi un campo SYMBOL che visualizza il carattere あ,
// con un carattere che supporta la pagina di codice Shift-JIS (Windows-932):
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Vedi anche

* Class [FieldSymbol](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
