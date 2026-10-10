---
title: "Classe Aspose::Words::Fields::FieldDisplayBarcode"
linktitle: "FieldDisplayBarcode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Fields::FieldDisplayBarcode. Implementa il campo DISPLAYBARCODE. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 34000
url: /it/cpp/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class


Implementa il campo DISPLAYBARCODE. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldDisplayBarcode : public Aspose::Words::Fields::Field,
                            public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | Ottiene o imposta se aggiungere i caratteri Inizio/Fine per i tipi di codice a barre NW7 e CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Ottiene o imposta il colore di sfondo del simbolo del codice a barre. I valori validi sono nell'intervallo [0, 0xFFFFFF]. |
| [get_BarcodeType](./get_barcodetype/)() | Ottiene o imposta il tipo di codice a barre (QR, ecc.). |
| [get_BarcodeValue](./get_barcodevalue/)() | Ottiene o imposta il valore del codice a barra. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets or sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_DisplayText](./get_displaytext/)() | Ottiene o imposta se visualizzare i dati del codice a barre (testo) insieme all'immagine. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | Ottiene o imposta il livello di correzione errori del QR Code. I valori validi sono [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Ottiene o imposta se correggere la cifra di controllo se è non valida. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Ottiene o imposta il colore di primo piano del simbolo del codice a barre. I valori validi sono nell'intervallo [0, 0xFFFFFF]. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets or sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_ScalingFactor](./get_scalingfactor/)() | Ottiene o imposta un fattore di scala per il simbolo. Il valore è espresso in punti percentuali interi e i valori validi sono [10, 1000]. |
| [get_Separator](../field/get_separator/)() | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_SymbolHeight](./get_symbolheight/)() | Ottiene o imposta l'altezza del simbolo. L'unità è in TWIPS (1/1440 di pollice). |
| [get_SymbolRotation](./get_symbolrotation/)() | Ottiene o imposta la rotazione del simbolo del codice a barre. I valori validi sono [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_AddStartStopChar](./get_addstartstopchar/). |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_BackgroundColor](./get_backgroundcolor/). |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeType](./get_barcodetype/). |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeValue](./get_barcodevalue/). |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_CaseCodeStyle](./get_casecodestyle/). |
| [set_DisplayText](./set_displaytext/)(bool) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_DisplayText](./get_displaytext/). |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_ErrorCorrectionLevel](./get_errorcorrectionlevel/). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_FixCheckDigit](./get_fixcheckdigit/). |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor](./get_foregroundcolor/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_PosCodeStyle](./get_poscodestyle/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_ScalingFactor](./get_scalingfactor/). |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolHeight](./get_symbolheight/). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolRotation](./get_symbolrotation/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |

## Esempi



Mostra come inserire un campo DISPLAYBARCODE e impostarne le proprietà.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));

// Di seguito sono riportati quattro tipi di codici a barre, decorati in vari modi, che il campo DISPLAYBARCODE può visualizzare.
// 1 -  QR code con colori personalizzati:
field->set_BarcodeType(u"QR");
field->set_BarcodeValue(u"ABC123");
field->set_BackgroundColor(u"0xF8BD69");
field->set_ForegroundColor(u"0xB5413B");
field->set_ErrorCorrectionLevel(u"3");
field->set_ScalingFactor(u"250");
field->set_SymbolHeight(u"1000");
field->set_SymbolRotation(u"0");

ASSERT_EQ(u" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field->GetFieldCode());
builder->Writeln();

// 2 -  Codice a barre EAN13, con le cifre visualizzate sotto le barre:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  Codice a barre CODE39:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  Codice a barre ITF4, con un codice di caso specificato:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.DISPLAYBARCODE.docx");
```

## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
