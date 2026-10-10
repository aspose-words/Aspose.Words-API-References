---
title: "Aspose::Words::Fields::IBarcodeGenerator gränssnitt"
linktitle: "IBarcodeGenerator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::IBarcodeGenerator gränssnitt. Publikt gränssnitt för anpassad streckkodsgenerator. Implementering bör tillhandahållas av användaren i C++."
type: docs
weight: 118000
url: /sv/cpp/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface


Publikt gränssnitt för anpassad streckkodsgenerator. Implementering bör tillhandahållas av användaren.

```cpp
class IBarcodeGenerator : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [GetBarcodeImage](./getbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Generera streckkodsbild med hjälp av uppsättningen parametrar (för DisplayBarcode-fältet). |
| virtual [GetOldBarcodeImage](./getoldbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Generera streckkodsbild med hjälp av uppsättningen parametrar (för det gammaldags Barcode-fältet). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
