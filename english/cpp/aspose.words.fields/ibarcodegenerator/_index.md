---
title: Aspose::Words::Fields::IBarcodeGenerator interface
linktitle: IBarcodeGenerator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::IBarcodeGenerator interface. Public interface for barcode custom generator. Implementation should be provided by user in C++.'
type: docs
weight: 118000
url: /cpp/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface


Public interface for barcode custom generator. Implementation should be provided by user.

```cpp
class IBarcodeGenerator : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [GetBarcodeImage](./getbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Generate barcode image using the set of parameters (for DisplayBarcode field). |
| virtual [GetOldBarcodeImage](./getoldbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Generate barcode image using the set of parameters (for old-fashioned Barcode field). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
