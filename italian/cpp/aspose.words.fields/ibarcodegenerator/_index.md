---
title: "Aspose::Words::Fields::IBarcodeGenerator interfaccia"
linktitle: "IBarcodeGenerator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::IBarcodeGenerator interfaccia. Interfaccia pubblica per un generatore personalizzato di codici a barre. L'implementazione dovrebbe essere fornita dall'utente in C++."
type: docs
weight: 118000
url: /it/cpp/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface


Interfaccia pubblica per il generatore personalizzato di codici a barre. L'implementazione dovrebbe essere fornita dall'utente.

```cpp
class IBarcodeGenerator : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [GetBarcodeImage](./getbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Genera l'immagine del codice a barre utilizzando il set di parametri (per il campo DisplayBarcode). |
| virtual [GetOldBarcodeImage](./getoldbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Genera l'immagine del codice a barre utilizzando il set di parametri (per il campo Barcode tradizionale). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
