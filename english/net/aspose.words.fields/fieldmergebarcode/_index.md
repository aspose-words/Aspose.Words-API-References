---
title: FieldMergeBarcode
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 1950
url: /net/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class

Implements the MERGEBARCODE field.

```csharp
public class FieldMergeBarcode : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldMergeBarcode](fieldmergebarcode)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/fieldmergebarcode/addstartstopchar) { get; set; } | Gets or sets whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [BackgroundColor](../../aspose.words.fields/fieldmergebarcode/backgroundcolor) { get; set; } | Gets or sets the background color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF] |
| [BarcodeType](../../aspose.words.fields/fieldmergebarcode/barcodetype) { get; set; } | Gets or sets the barcode type (QR, etc.) |
| [BarcodeValue](../../aspose.words.fields/fieldmergebarcode/barcodevalue) { get; set; } | Gets or sets the barcode value. |
| [CaseCodeStyle](../../aspose.words.fields/fieldmergebarcode/casecodestyle) { get; set; } | Gets or sets the style of a Case Code for barcode type ITF14. The valid values are [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Gets the text that represents the displayed field result. |
| [DisplayText](../../aspose.words.fields/fieldmergebarcode/displaytext) { get; set; } | Gets or sets whether to display barcode data (text) along with image. |
| [End](../../aspose.words.fields/field/end) { get; } | Gets the node that represents the field end. |
| [ErrorCorrectionLevel](../../aspose.words.fields/fieldmergebarcode/errorcorrectionlevel) { get; set; } | Gets or sets an error correction level of QR Code. Valid values are [0, 3]. |
| [FixCheckDigit](../../aspose.words.fields/fieldmergebarcode/fixcheckdigit) { get; set; } | Gets or sets whether to fix the check digit if it’s invalid. |
| [ForegroundColor](../../aspose.words.fields/fieldmergebarcode/foregroundcolor) { get; set; } | Gets or sets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF] |
| [Format](../../aspose.words.fields/field/format) { get; } | Gets a [`FieldFormat`](../fieldformat) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Gets or sets the LCID of the field. |
| [PosCodeStyle](../../aspose.words.fields/fieldmergebarcode/poscodestyle) { get; set; } | Gets or sets the style of a Point of Sale barcode (barcode types UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). The valid values (case insensitive) are [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [ScalingFactor](../../aspose.words.fields/fieldmergebarcode/scalingfactor) { get; set; } | Gets or sets a scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000] |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Gets the node that represents the field separator. Can be null. |
| [Start](../../aspose.words.fields/field/start) { get; } | Gets the node that represents the start of the field. |
| [SymbolHeight](../../aspose.words.fields/fieldmergebarcode/symbolheight) { get; set; } | Gets or sets the height of the symbol. The units are in TWIPS (1/1440 inch). |
| [SymbolRotation](../../aspose.words.fields/fieldmergebarcode/symbolrotation) { get; set; } | Gets or sets the rotation of the barcode symbol. Valid values are [0, 3] |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Gets the Microsoft Word field type. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [Unlink](../../aspose.words.fields/field/unlink)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update)(bool) | Performs a field update. Throws if the field is being updated already. |

### Remarks

Mail merge a barcode.

### See Also

* class [Field](../field)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
