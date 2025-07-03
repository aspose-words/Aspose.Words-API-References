---
title: Aspose::Words::Fields::FieldMergeBarcode class
linktitle: FieldMergeBarcode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldMergeBarcode class. Implements the MERGEBARCODE field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 66000
url: /cpp/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class


Implements the MERGEBARCODE field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldMergeBarcode : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Methods

| Method | Description |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | Gets whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Gets the background color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]. |
| [get_BarcodeType](./get_barcodetype/)() | Gets the barcode type (QR, etc.) |
| [get_BarcodeValue](./get_barcodevalue/)() | Gets the barcode value. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets the style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_DisplayText](./get_displaytext/)() | Gets whether to display barcode data (text) along with image. |
| [get_End](./get_end/)() override | Gets the node that represents the field end. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | Gets an error correction level of QR Code. Valid values are [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Gets whether to fix the check digit if it’s invalid. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Gets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE]. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_ScalingFactor](./get_scalingfactor/)() | Gets a scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]. |
| [get_Separator](./get_separator/)() override | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](./get_start/)() override | Gets the node that represents the start of the field. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_SymbolHeight](./get_symbolheight/)() | Gets the height of the symbol. The units are in TWIPS (1/1440 inch). |
| [get_SymbolRotation](./get_symbolrotation/)() | Gets the rotation of the barcode symbol. Valid values are [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Sets whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Sets the background color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]. |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Sets the barcode type (QR, etc.) |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Sets the barcode value. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Sets the style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Sets whether to display barcode data (text) along with image. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Sets an error correction level of QR Code. Valid values are [0, 3]. |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Sets whether to fix the check digit if it’s invalid. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Sets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF]. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Sets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE]. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Sets a scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Sets the height of the symbol. The units are in TWIPS (1/1440 inch). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Sets the rotation of the barcode symbol. Valid values are [0, 3]. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
