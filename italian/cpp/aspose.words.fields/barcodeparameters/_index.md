---
title: "Aspose::Words::Fields::BarcodeParameters class"
linktitle: "BarcodeParameters"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::BarcodeParameters class. Classe contenitore per i parametri del codice a barre da passare a BarcodeGenerator. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class


Classe contenitore per i parametri del codice a barre da passare a BarcodeGenerator. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class BarcodeParameters : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [BarcodeParameters](./barcodeparameters/)() |  |
| [get_AddStartStopChar](./get_addstartstopchar/)() const | Indica se aggiungere i caratteri Start/Stop per i tipi di codice a barre NW7 e CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() const | Colore di sfondo del codice a barre (0x000000 - 0xFFFFFF) |
| [get_BarcodeType](./get_barcodetype/)() const | Tipo di codice a barre. |
| [get_BarcodeValue](./get_barcodevalue/)() const | Dati da codificare. |
| [get_CaseCodeStyle](./get_casecodestyle/)() const | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayText](./get_displaytext/)() const | Indica se visualizzare i dati del codice a barre (testo) insieme all'immagine. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() const | Livello di correzione errori del QR Code. I valori validi sono [0, 3]. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() const | Tipo di Marchio di Identificazione Frontale (FIM). |
| [get_FixCheckDigit](./get_fixcheckdigit/)() const | Indica se correggere la cifra di controllo se è non valida. |
| [get_ForegroundColor](./get_foregroundcolor/)() const | Colore di primo piano del codice a barre (0x000000 - 0xFFFFFF) |
| [get_IsBookmark](./get_isbookmark/)() const | Indica se [PostalAddress](./get_postaladdress/) è il nome di un segnalibro. |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() const | Indica se [PostalAddress](./get_postaladdress/) è un indirizzo postale degli Stati Uniti. |
| [get_PosCodeStyle](./get_poscodestyle/)() const | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_PostalAddress](./get_postaladdress/)() const | Indirizzo postale del codice a barre. |
| [get_ScalingFactor](./get_scalingfactor/)() const | Fattore di scala per il simbolo. Il valore è espresso in punti percentuali interi e i valori validi sono [10, 1000]. |
| [get_SymbolHeight](./get_symbolheight/)() const | Altezza dell'immagine del codice a barre (in twip - 1/1440 pollici) |
| [get_SymbolRotation](./get_symbolrotation/)() const | Rotazione del simbolo del codice a barre. I valori validi sono [0, 3]. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Indica se aggiungere i caratteri Start/Stop per i tipi di codice a barre NW7 e CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Colore di sfondo del codice a barre (0x000000 - 0xFFFFFF) |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Tipo di codice a barre. |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Dati da codificare. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Indica se visualizzare i dati del codice a barre (testo) insieme all'immagine. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Livello di correzione errori del QR Code. I valori validi sono [0, 3]. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | Tipo di Marchio di Identificazione Frontale (FIM). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Indica se correggere la cifra di controllo se è non valida. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Colore di primo piano del codice a barre (0x000000 - 0xFFFFFF) |
| [set_IsBookmark](./set_isbookmark/)(bool) | Indica se [PostalAddress](./get_postaladdress/) è il nome di un segnalibro. |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | Indica se [PostalAddress](./get_postaladdress/) è un indirizzo postale degli Stati Uniti. |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | Indirizzo postale del codice a barre. |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Fattore di scala per il simbolo. Il valore è espresso in punti percentuali interi e i valori validi sono [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Altezza dell'immagine del codice a barre (in twip - 1/1440 pollici) |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Rotazione del simbolo del codice a barre. I valori validi sono [0, 3]. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
