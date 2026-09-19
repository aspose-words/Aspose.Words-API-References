---
title: "Aspose::Words::Fields::FieldMergeBarcode classe"
linktitle: "FieldMergeBarcode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldMergeBarcode classe. Implementa il campo MERGEBARCODE. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 66000
url: /it/cpp/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class


Implementa il campo MERGEBARCODE. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldMergeBarcode : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | Ottiene se aggiungere i caratteri Start/Stop per i tipi di codice a barre NW7 e CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Ottiene il colore di sfondo del simbolo del codice a barre. I valori validi sono nell'intervallo [0, 0xFFFFFF]. |
| [get_BarcodeType](./get_barcodetype/)() | Ottiene il tipo di codice a barre (QR, ecc.) |
| [get_BarcodeValue](./get_barcodevalue/)() | Ottiene il valore del codice a barre. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Restituisce il testo che rappresenta il risultato del campo visualizzato. |
| [get_DisplayText](./get_displaytext/)() | Ottiene se visualizzare i dati del codice a barre (testo) insieme all'immagine. |
| [get_End](./get_end/)() override | Restituisce il nodo che rappresenta la fine del campo. |
| [get_End](../field/get_end/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | Ottiene il livello di correzione degli errori del QR Code. I valori validi sono [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | Restituisce il nodo che rappresenta la fine del campo. |
| [get_FieldStart](../field/get_fieldstart/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Ottiene se correggere la cifra di controllo se è invalida. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Ottiene il colore di primo piano del simbolo del codice a barre. I valori validi sono nell'intervallo [0, 0xFFFFFF]. |
| [get_Format](../field/get_format/)() | Restituisce un oggetto [FieldFormat](../fieldformat/) che fornisce un accesso tipizzato alla formattazione del campo. |
| [get_IsDirty](../field/get_isdirty/)() | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsLocked](../field/get_islocked/)() | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_LocaleId](../field/get_localeid/)() | Ottiene o imposta il LCID del campo. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | Ottiene o imposta il testo che si trova tra il separatore del campo e la fine del campo. |
| [get_ScalingFactor](./get_scalingfactor/)() | Ottiene un fattore di scala per il simbolo. Il valore è espresso in punti percentuali interi e i valori validi sono [10, 1000]. |
| [get_Separator](./get_separator/)() override | Restituisce il nodo che rappresenta il separatore del campo. Può essere **null**. |
| [get_Start](./get_start/)() override | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_Start](../field/get_start/)() const | Restituisce il nodo che rappresenta l'inizio del campo. |
| [get_SymbolHeight](./get_symbolheight/)() | Ottiene l'altezza del simbolo. L'unità è in TWIPS (1/1440 di pollice). |
| [get_SymbolRotation](./get_symbolrotation/)() | Ottiene la rotazione del simbolo del codice a barre. I valori validi sono [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | Restituisce il tipo di campo di Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). Sono inclusi sia il codice del campo sia il risultato dei campi figlio. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce **null**. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Imposta se aggiungere i caratteri Start/Stop per i tipi di codice a barre NW7 e CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Imposta il colore di sfondo del simbolo del codice a barre. I valori validi sono nell'intervallo [0, 0xFFFFFF]. |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Imposta il tipo di codice a barre (QR, ecc.) |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Imposta il valore del codice a barre. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Imposta se visualizzare i dati del codice a barre (testo) insieme all'immagine. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Imposta il livello di correzione degli errori del QR Code. I valori validi sono [0, 3]. |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Imposta se correggere la cifra di controllo se è invalida. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Imposta il colore di primo piano del simbolo del codice a barre. I valori validi sono nell'intervallo [0, 0xFFFFFF]. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter per [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter per [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter per [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Imposta un fattore di scala per il simbolo. Il valore è in punti percentuali interi e i valori validi sono [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Imposta l'altezza del simbolo. L'unità è in TWIPS (1/1440 di pollice). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Imposta la rotazione del simbolo del codice a barre. I valori validi sono [0, 3]. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../field/update/)() | Esegue l'aggiornamento del campo. Lancia un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../field/update/)(bool) | Esegue un aggiornamento del campo. Lancia un'eccezione se il campo è già in aggiornamento. |
## Vedi anche

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
