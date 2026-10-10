---
title: "Aspose::Words::Fields::BarcodeParameters klass"
linktitle: "BarcodeParameters"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::BarcodeParameters klass. Behållarklass för streckkodparametrar att vidarebefordra till BarcodeGenerator. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class


Behållarklass för streckkodparametrar som ska vidarebefordras till BarcodeGenerator. För att lära dig mer, besök [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokumentationsartikel.

```cpp
class BarcodeParameters : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [BarcodeParameters](./barcodeparameters/)() |  |
| [get_AddStartStopChar](./get_addstartstopchar/)() const | Om Start/Stop-tecken ska läggas till för streckkodstyperna NW7 och CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() const | Bakgrundsfärg för streckkod (0x000000 - 0xFFFFFF) |
| [get_BarcodeType](./get_barcodetype/)() const | Streckkodstyp. |
| [get_BarcodeValue](./get_barcodevalue/)() const | Data som ska kodas. |
| [get_CaseCodeStyle](./get_casecodestyle/)() const | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayText](./get_displaytext/)() const | Om streckkodsdata (text) ska visas tillsammans med bilden. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() const | Felkorrigeringsnivå för QR-kod. Giltiga värden är [0, 3]. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() const | Typ av Facing Identification Mark (FIM). |
| [get_FixCheckDigit](./get_fixcheckdigit/)() const | Om kontrollsiffran ska korrigeras om den är ogiltig. |
| [get_ForegroundColor](./get_foregroundcolor/)() const | Förgrundsfärg för streckkod (0x000000 - 0xFFFFFF) |
| [get_IsBookmark](./get_isbookmark/)() const | Om [PostalAddress](./get_postaladdress/) är namnet på ett bokmärke. |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() const | Om [PostalAddress](./get_postaladdress/) är en amerikansk postadress. |
| [get_PosCodeStyle](./get_poscodestyle/)() const | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_PostalAddress](./get_postaladdress/)() const | Streckkodens postadress. |
| [get_ScalingFactor](./get_scalingfactor/)() const | Skalningsfaktor för symbolen. Värdet är i hela procentenheter och giltiga värden är [10, 1000]. |
| [get_SymbolHeight](./get_symbolheight/)() const | Höjd på streckkodens bild (i twips - 1/1440 tum) |
| [get_SymbolRotation](./get_symbolrotation/)() const | Rotation av streckkodssymbolen. Giltiga värden är [0, 3]. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Om Start/Stop-tecken ska läggas till för streckkodstyperna NW7 och CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Bakgrundsfärg för streckkod (0x000000 - 0xFFFFFF) |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Streckkodstyp. |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Data som ska kodas. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Om streckkodsdata (text) ska visas tillsammans med bilden. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Felkorrigeringsnivå för QR-kod. Giltiga värden är [0, 3]. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | Typ av Facing Identification Mark (FIM). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Om kontrollsiffran ska korrigeras om den är ogiltig. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Förgrundsfärg för streckkod (0x000000 - 0xFFFFFF) |
| [set_IsBookmark](./set_isbookmark/)(bool) | Om [PostalAddress](./get_postaladdress/) är namnet på ett bokmärke. |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | Om [PostalAddress](./get_postaladdress/) är en amerikansk postadress. |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | Streckkodens postadress. |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Skalningsfaktor för symbolen. Värdet är i hela procentenheter och giltiga värden är [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Höjd på streckkodens bild (i twips - 1/1440 tum) |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Rotation av streckkodssymbolen. Giltiga värden är [0, 3]. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
