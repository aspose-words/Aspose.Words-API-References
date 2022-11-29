---
title: IBarcodeGenerator
second_title: Aspose.Words for C++ API Reference
description: Public interface for barcode custom generator. Implementation should be provided by user.
type: docs
weight: 1509
url: /cpp/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface


Public interface for barcode custom generator. Implementation should be provided by user.

```cpp
class IBarcodeGenerator : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [GetBarcodeImage](./getbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Generate barcode image using the set of parameters (for DisplayBarcode field). |
| virtual [GetOldBarcodeImage](./getoldbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Generate barcode image using the set of parameters (for old-fashioned Barcode field). |
## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words](../../)
