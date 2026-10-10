---
title: "Aspose::Words::Fields::IBarcodeGenerator Schnittstelle"
linktitle: "IBarcodeGenerator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::IBarcodeGenerator Schnittstelle. Öffentliche Schnittstelle für benutzerdefinierten Barcode-Generator. Die Implementierung sollte vom Benutzer in C++ bereitgestellt werden."
type: docs
weight: 118000
url: /de/cpp/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface


Öffentliche Schnittstelle für benutzerdefinierten Barcode-Generator. Die Implementierung sollte vom Benutzer bereitgestellt werden.

```cpp
class IBarcodeGenerator : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [GetBarcodeImage](./getbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Barcode-Bild mit dem Satz von Parametern erzeugen (für das DisplayBarcode-Feld). |
| virtual [GetOldBarcodeImage](./getoldbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Barcode-Bild mit dem Satz von Parametern erzeugen (für das altmodische Barcode-Feld). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
