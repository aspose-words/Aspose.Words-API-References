---
title: "Aspose::Words::Fields::FieldSymbol classe"
linktitle: "FieldSymbol"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldSymbol classe. Implementa un campo SYMBOL. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 98000
url: /it/cpp/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class


Implementa un campo SYMBOL. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldSymbol : public Aspose::Words::Fields::Field,
                    public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_CharacterCode](./get_charactercode/)() | Ottiene o imposta il valore del punto di codice del carattere in decimale o esadecimale. |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_DontAffectsLineSpacing](./get_dontaffectslinespacing/)() | Ottiene o imposta se il carattere recuperato dal campo influisce sull'interlinea del paragrafo. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_FontName](./get_fontname/)() | Ottiene o imposta il nome del font del carattere recuperato dal campo. |
| [get_FontSize](./get_fontsize/)() | Ottiene o imposta la dimensione in punti del font del carattere recuperato dal campo. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IsAnsi](./get_isansi/)() | Ottiene o imposta se il codice del carattere è interpretato come valore di un carattere ANSI. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_IsShiftJis](./get_isshiftjis/)() | Ottiene o imposta se il codice del carattere è interpretato come valore di un carattere SHIFT-JIS. |
| [get_IsUnicode](./get_isunicode/)() | Ottiene o imposta se il codice del carattere è interpretato come valore di un carattere Unicode. |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_CharacterCode](./set_charactercode/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldSymbol::get_CharacterCode](./get_charactercode/). |
| [set_DontAffectsLineSpacing](./set_dontaffectslinespacing/)(bool) | Impostatore per [Aspose::Words::Fields::FieldSymbol::get_DontAffectsLineSpacing](./get_dontaffectslinespacing/). |
| [set_FontName](./set_fontname/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldSymbol::get_FontName](./get_fontname/). |
| [set_FontSize](./set_fontsize/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldSymbol::get_FontSize](./get_fontsize/). |
| [set_IsAnsi](./set_isansi/)(bool) | Impostatore per [Aspose::Words::Fields::FieldSymbol::get_IsAnsi](./get_isansi/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsShiftJis](./set_isshiftjis/)(bool) | Impostatore per [Aspose::Words::Fields::FieldSymbol::get_IsShiftJis](./get_isshiftjis/). |
| [set_IsUnicode](./set_isunicode/)(bool) | Impostatore per [Aspose::Words::Fields::FieldSymbol::get_IsUnicode](./get_isunicode/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
