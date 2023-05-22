---
title: Aspose::Words::Fields::BarcodeParameters class
linktitle: BarcodeParameters
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::BarcodeParameters class. Container class for barcode parameters to pass-through to BarcodeGenerator. To learn more, visit the  documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class


Container class for barcode parameters to pass-through to BarcodeGenerator. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class BarcodeParameters : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [BarcodeParameters](./barcodeparameters/)() |  |
| [get_AddStartStopChar](./get_addstartstopchar/)() const | Whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() const | Bar code background color (0x000000 - 0xFFFFFF) |
| [get_BarcodeType](./get_barcodetype/)() const | Bar code type. |
| [get_BarcodeValue](./get_barcodevalue/)() const | Data to be encoded. |
| [get_CaseCodeStyle](./get_casecodestyle/)() const | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]. |
| [get_DisplayText](./get_displaytext/)() const | Whether to display barcode data (text) along with image. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() const | Error correction level of QR Code. Valid values are [0, 3]. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() const | Type of a Facing Identification Mark (FIM). |
| [get_FixCheckDigit](./get_fixcheckdigit/)() const | Whether to fix the check digit if it’s invalid. |
| [get_ForegroundColor](./get_foregroundcolor/)() const | Bar code foreground color (0x000000 - 0xFFFFFF) |
| [get_IsBookmark](./get_isbookmark/)() const | Whether [PostalAddress](./get_postaladdress/) is the name of a bookmark. |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() const | Whether [PostalAddress](./get_postaladdress/) is a U.S. postal address. |
| [get_PosCodeStyle](./get_poscodestyle/)() const | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE]. |
| [get_PostalAddress](./get_postaladdress/)() const | Barcode postal address. |
| [get_ScalingFactor](./get_scalingfactor/)() const | Scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]. |
| [get_SymbolHeight](./get_symbolheight/)() const | Bar code image height (in twips - 1/1440 inches) |
| [get_SymbolRotation](./get_symbolrotation/)() const | Rotation of the barcode symbol. Valid values are [0, 3]. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Bar code background color (0x000000 - 0xFFFFFF) |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Bar code type. |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Data to be encoded. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Whether to display barcode data (text) along with image. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Error correction level of QR Code. Valid values are [0, 3]. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | Type of a Facing Identification Mark (FIM). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Whether to fix the check digit if it’s invalid. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Bar code foreground color (0x000000 - 0xFFFFFF) |
| [set_IsBookmark](./set_isbookmark/)(bool) | Whether [PostalAddress](./get_postaladdress/) is the name of a bookmark. |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | Whether [PostalAddress](./get_postaladdress/) is a U.S. postal address. |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE]. |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | Barcode postal address. |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Bar code image height (in twips - 1/1440 inches) |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Rotation of the barcode symbol. Valid values are [0, 3]. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
